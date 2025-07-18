# CrewAI Research Project

The CrewAI project is designed to leverage advanced web search capabilities for real-time research, data gathering, and comprehensive reporting. It integrates the SerperDevTool to perform web searches and gather up-to-date information from the internet. The project is configured to ensure that sensitive information like API keys is managed securely.

## Project Purpose

The CrewAI project aims to enhance research and reporting capabilities using automated agents equipped with state-of-the-art web search tools. The project provides:

- **Web Search Integration**: Uses the SerperDevTool for accessing real-time web data 
- **Real-time Research**: Collects and analyzes the latest developments and trends 
- **Comprehensive Reporting**: Transforms data into detailed, structured reports

## Setup Instructions

### Prerequisites

- Python 3.10.x to 3.13.x
- A virtual environment is recommended for installing dependencies

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Create a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Configuration

1. **API Keys**: 

   Add your SerperDev API key to the `.env` file in the project root:
   ```
   SERPER_API_KEY=<YOUR_SERPER_API_KEY>
   OPENAI_API_KEY=<YOUR_OPENAI_API_KEY>
   ```

2. **Environment Variables**:

   Ensure that your `.env` file contains all necessary API keys. These are accessed within the code using `os.getenv`.

### Usage

To run the CrewAI application, use the following command:
```bash
crewai run
```

This will activate the research task that leverages web search capabilities to provide comprehensive and up-to-date insights on the specified topics.

## SerperDevTool Integration

The SerperDevTool is an integral part of the CrewAI project, adding powerful web search functionality. This tool is initialized in the `research_task` function within `crew.py`, which requires the previously configured API key.

### Usage in Research Tasks

- Searches the web to gather the latest information
- Integrates data into research outputs with sources and links
- Used by the 'researcher' agent defined in `agents.yaml`

## Managing Sensitive Information

Sensitive information such as API keys must be handled securely.

- **Do not hardcode keys**: Use environment variables to load API keys.
  
- **Environment Configuration**: Store your configurations in the `.env` file and ensure it is included in your `.gitignore` to avoid accidental exposure.

## Conclusion

The CrewAI research project streamlines the process of gathering and reporting up-to-date web data. Its agent-driven framework facilitates efficient information processing and reporting while maintaining secure handling of sensitive information.
