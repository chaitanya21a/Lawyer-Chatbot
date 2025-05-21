# ⚖️ Lawyer Chatbot

An AI-powered legal assistant that uses **Retrieval-Augmented Generation (RAG)** to answer questions from uploaded legal PDF documents. It combines document retrieval with powerful language models to provide accurate and contextual answers.

---
> 💡 **Note:** This project requires the `deepseek-r1-distill-llama-70b` model to be installed locally using [Ollama](https://ollama.com/).  
> You can install it by running:  
> ```bash
> ollama pull deepseek-r1-distill-llama-70b
> ```
---

## 📑 Table of Contents

1. [Project Overview](#project-overview)  
2. [Environment Setup](#environment-setup)  
   - [Using Pipenv](#using-pipenv)  
   - [Using Conda](#using-conda)  
   - [Using Pip](#using-pip)  
3. [Running the Project](#running-the-project)  

---

## 🧠 Project Overview

This project consists of three main components:

- `frontend.py`: The user-facing Streamlit app to interact with the chatbot.
- `vector_database.py`: Sets up the FAISS vector database for document retrieval.
- `rag_pipeline.py`: Implements the core RAG logic that retrieves and answers questions.

Users can upload a legal PDF and ask questions. The system fetches relevant context from the document and uses an LLM to generate accurate legal responses.

<Image src="/image.png" alt="Cartoon AI Lawyer" width={300} />

---

## Environment Setup

### Using Pipenv
Pipenv is a tool that manages dependencies and virtual environments for Python projects.

1. Install Pipenv if you don't have it:
    ```
    pip install pipenv
    ```

2. Navigate to the project directory and create a virtual environment:
    ```
    pipenv install
    ```

3. Activate the virtual environment:
    ```
    pipenv shell
    ```

4. (Optional) Install any additional dependencies:
    ```
    pipenv install <package_name>
    ```

---

### Using Conda
Conda is an open-source package management system and environment management system.

1. Create a new conda environment:
    ```
    conda create -n myenv python=3.9
    ```

2. Activate the environment:
    ```
    conda activate myenv
    ```

3. Install dependencies from `requirements.txt` (if available):
    ```
    pip install -r requirements.txt
    ```

---

### Using Pip
Pip is the standard package installer for Python.

1. Install virtualenv if you don't have it:
    ```
    pip install virtualenv
    ```

2. Create a virtual environment:
    ```
    virtualenv venv
    ```

3. Activate the virtual environment:
    - On Windows:
        ```
        venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```
        source venv/bin/activate
        ```

4. Install dependencies from `requirements.txt` (if available):
    ```
    pip install -r requirements.txt
    ```

---

## Running the Project

The project consists of three Python files, each corresponding to a different phase of the project:

### To run the App directly
```
streamlit run main.py
```

### To run app in different phases

1. Phase 1: Run the first phase using:
    ```
    streamlit run frontend.py
    ```

2. Phase 2: Run the second phase using:
    ```
    python vector_database.py
    ```

3. Phase 3: Run the third phase using:
    ```
    python rag_pipeline.py
    ```

Ensure that all dependencies are installed before running the scripts.

---

If you encounter any issues, feel free to reach out or check the documentation for the tools mentioned above.