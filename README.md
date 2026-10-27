# customer-support-rag

# Customer Support RAG API

## Overview
A Retrieval-Augmented Generation (RAG) based customer support system that answers user queries using a predefined FAQ knowledge base.

## Tech Stack
- Python
- FastAPI
- LangChain
- LangGraph
- FAISS vector database
- Hugging Face Sentence Transformers
- Ollama (LLM backend)

## Project Structure
- `app.py` — FastAPI application and API endpoints
- `support_rag.py` — RAG pipeline, retrieval, and response generation
- `support_faq.txt` — Customer support knowledge base
- `requirements.txt` — Python dependencies
- `.env.example` — Example configuration

## Setup and Execution

1. Clone the repository:
   `git clone YOUR_REPOSITORY_URL`

2. Navigate to the project directory:
   `cd customer-support-rag`

3. Install dependencies:
   `pip install -r requirements.txt`

4. Install and start Ollama, then download the configured model:
   `ollama pull qwen2.5:0.5b`

5. Start the API:
   `uvicorn app:app --reload`

6. Open the interactive API documentation:
   `http://127.0.0.1:8000/docs`

## API Endpoints
- `GET /health` — Check API health
- `POST /ask` — Submit a customer support question

## Notes
The application retrieves relevant information from the FAQ knowledge base before generating an answer. Configure the LLM backend using environment variables as required.
