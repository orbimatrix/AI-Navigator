# 🤖 PDF Analysis with CrewAI - Streamlit Application

A powerful Streamlit application that uses AI agents to analyze PDF documents, generate insights, and provide comprehensive project analysis using CrewAI.

## 🚀 Features

- **PDF Upload & Analysis**: Upload any PDF and get AI-powered analysis
- **Multi-Agent System**: Three specialized AI agents working together
  - Project Analyst: Identifies risks, strengths, and opportunities
  - Resource Search Specialist: Discovers relevant tools and resources
  - Code Architect: Designs system architecture and generates code
- **Real-time Results**: See analysis progress and results in real-time
- **File Generation**: Automatically generates markdown reports and documentation
- **Download Capability**: Download all generated files for offline use

## 📋 Prerequisites

Before running this application, make sure you have:

- **Python 3.8+** installed on your system
- **Git** for version control
- **GitHub account** for hosting the repository
- **API Keys** for the required services (see Setup section)

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
# Clone the repository to your local machine
git clone https://github.com/yourusername/pdf-analysis-crewai.git

# Navigate to the project directory
cd pdf-analysis-crewai
```

### 2. Create Virtual Environment (Recommended)

```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On Windows:
venv\Scripts\activate

# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

```bash
# Install all required packages
pip install -r requirements.txt
```

### 4. Environment Configuration

Create a `.env` file in the root directory with your API keys:

```env
# Required: Your AIML API key for GPT-5 access
AIML_API_KEY=your_aiml_api_key_here

# Optional: GitHub token for enhanced repository search
GITHUB_TOKEN=your_github_token_here

# Optional: Linkup API key for additional search capabilities
LINKUP_API_KEY=your_linkup_api_key_here

# Optional: EXA API key for scientific research
EXA_API_KEY=your_exa_api_key_here
```

**Note**: Only `AIML_API_KEY` is required. Other keys are optional but enhance functionality.

## 🚀 Running the Application

### Option 1: Direct Streamlit Run

```bash
# Make sure your virtual environment is activated
streamlit run streamlit_app.py
```

### Option 2: Using Python Module

```bash
# Alternative way to run
python -m streamlit run streamlit_app.py
```

### Option 3: Development Mode

```bash
# Run with auto-reload for development
streamlit run streamlit_app.py --server.runOnSave true
```

## 🌐 Accessing the Application

Once running, the application will be available at:
- **Local**: http://localhost:8501
- **Network**: http://your-ip-address:8501

The app will automatically open in your default web browser.

## 📱 How to Use

1. **Upload PDF**: Use the file uploader to select a PDF document
2. **Start Analysis**: Click the "🚀 Start AI Analysis" button
3. **Wait for Results**: Monitor the progress as AI agents analyze your document
4. **View Results**: See the analysis results and generated files
5. **Check Files**: Click "🔄 Check Generated Files" to refresh and see new content
6. **Download**: Download any generated markdown files for offline use

## 📁 Generated Output

The application creates three main output directories:

- **`project_analysis_output/`**: Project analysis reports and insights
- **`resource_output/`**: Resource discovery findings and recommendations
- **`code_output/`**: System architecture and code generation outputs

## 🔧 Troubleshooting

### Common Issues

1. **"No generated files found"**
   - Click "🔄 Check Generated Files" button
   - Wait a few minutes for agents to complete processing
   - Check console for any error messages

2. **API Key Errors**
   - Verify your `.env` file is in the root directory
   - Ensure `AIML_API_KEY` is correctly set
   - Check that the API key is valid and has sufficient credits

3. **PDF Reading Errors**
   - Ensure the PDF is not password-protected
   - Try with a different PDF file
   - Check if the PDF contains extractable text (not just images)

4. **Port Already in Use**
   - Streamlit will automatically use the next available port
   - Check the terminal output for the actual port number

### Getting Help

- Check the terminal/console for detailed error messages
- Verify all dependencies are installed correctly
- Ensure your virtual environment is activated

## 📤 Uploading to GitHub

### 1. Initialize Git Repository (if not already done)

```bash
# Initialize git repository
git init

# Add all files to git
git add .

# Make initial commit
git commit -m "Initial commit: PDF Analysis with CrewAI Streamlit app"
```

### 2. Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `pdf-analysis-crewai`)
5. Add a description
6. Choose public or private
7. **DO NOT** initialize with README, .gitignore, or license (we already have these)
8. Click "Create repository"

### 3. Connect and Push to GitHub

```bash
# Add the remote origin (replace with your repository URL)
git remote add origin https://github.com/yourusername/pdf-analysis-crewai.git

# Push to GitHub
git push -u origin main

# If your default branch is 'master' instead of 'main':
git push -u origin master
```

### 4. Verify Upload

- Go to your GitHub repository
- Verify all files are uploaded correctly
- Check that the README.md is properly displayed

## 🔄 Updating the Repository

When you make changes to your code:

```bash
# Add all changes
git add .

# Commit changes with a descriptive message
git commit -m "Update: Improved file generation and error handling"

# Push to GitHub
git push origin main
```

## 📚 Project Structure

```
pdf-analysis-crewai/
├── streamlit_app.py          # Main Streamlit application
├── requirements.txt          # Python dependencies
├── README.md                # This file
├── .env                     # Environment variables (create this)
├── .gitignore              # Git ignore file
├── project_analysis_output/ # Generated project analysis files
├── resource_output/         # Generated resource discovery files
└── code_output/            # Generated architecture and code files
```

## 🌟 Customization

### Adding New Agents

To add new AI agents:

1. Create a new agent in the `create_agents()` function
2. Define corresponding tasks in `create_tasks()`
3. Update the crew configuration
4. Add new output folders if needed

### Modifying Output Formats

- Edit the task descriptions to change output requirements
- Modify the file reading logic in `safe_read_file()`
- Update the UI display logic in the main function

### Styling Changes

- Modify the CSS in the `st.markdown()` sections
- Update page configuration in `st.set_page_config()`
- Customize the sidebar and main content layout

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **CrewAI**: For the powerful multi-agent framework
- **Streamlit**: For the excellent web application framework
- **OpenAI**: For the GPT-5 language model
- **Community**: For contributions and feedback

## 📞 Support

If you encounter any issues or have questions:

1. Check the troubleshooting section above
2. Search existing GitHub issues
3. Create a new issue with detailed information
4. Include error messages and steps to reproduce

---

**Happy PDF Analyzing! 🚀📚🤖**
