# BonBon FAQ Chatbot Assignment

This project demonstrates how to build a context-aware chatbot for customer support using LangChain, Azure OpenAI, and Chroma vector database. The chatbot indexes a sample FAQ PDF and can answer user questions by retrieving relevant information from the document or searching the internet.

## Project Structure

- `assignment.ipynb`: Main notebook containing all code and instructions for the assignment.
- `data/BonBon FAQ.pdf`: Sample FAQ document to be indexed and used as the knowledge base.

## Setup Instructions

### 1. Prerequisites
- Windows Subsystem for Linux (WSL)
- Miniconda3

### 2. Environment Setup
- Create a new conda environment:
  ```sh
  conda create -n langchain python=3.11
  ```
- Activate the environment and set it as the Python interpreter in VS Code.

### 3. Install Required Packages
Run the following commands in a notebook cell or terminal:
```sh
pip install python-dotenv langchain openai chromadb tiktoken pypdf duckduckgo-search langchain-community langchain-openai scikit-learn
```

### 4. Environment Variables
Create a `.env` file in the project root with the following variables (get values from your training team):
```
OPENAI_API_KEY=your_openai_api_key
OPENAI_API_BASE=your_openai_api_base
OPENAI_API_VERSION=your_openai_api_version
OPENAI_API_DELOYMENT_NAME=your_azure_deployment_name
OPENAI_API_MODEL_NAME=your_azure_model_name
AZURE_OPENAI_ENDPOINT=your_azure_endpoint
OPENAI_API_CHAT_DEPLOYMENT_NAME=your_azure_chat_deployment_name
OPENAI_API_CHAT_MODEL_NAME=your_azure_chat_model_name
```

## Assignment Overview

### Assignment 1: Document Indexing
- Index the content of `BonBon FAQ.pdf` into a local Chroma vector database using an embedding model (e.g., Azure OpenAI text-embedding-ada-002).

### Assignment 2: Build the Chatbot
- Implement a chatbot using LangChain's Conversational ReAct agent.
- The chatbot answers questions using the indexed FAQ or, if not found, via DuckDuckGo internet search.
- Answers should cite the source file and page number when using the FAQ.

### Assignment 3: (Optional)
- Index the FAQ to Azure Cognitive Search and build a new assistant with similar behavior.

## Usage
- Open `assignment.ipynb` in VS Code.
- Follow the notebook cells to set up the environment, index the FAQ, and interact with the chatbot.
- Run the chatbot and ask questions related to IT support, networking, software, or hardware issues.

## Contact
For questions or to obtain the BonBon source code, contact the training team.

## Acknowledgments
Special thanks to AI tools like GitHub Copilot and ChatGPT, which provided valuable assistance and guidance throughout the development of this assignment. These tools helped streamline the coding process, suggest implementation approaches, and debug issues, enabling the successful completion of this project.