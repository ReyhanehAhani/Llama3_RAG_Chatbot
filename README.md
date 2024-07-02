# RAG Chatbot

This project implements a Retrieval-Augmented Generation (RAG) chatbot system using LangChain and LangGraph. The chatbot is designed to answer queries related to Computer Science and Natural Language Processing (NLP).

## Features

- Document retrieval using both vector store and search engine
- Relevance checking of retrieved documents
- Fallback mechanism for out-of-domain queries
- LangGraph workflow for orchestrating the RAG process
- Gradio interface for easy interaction with the chatbot

## Components

1. **Data Loading**: Loads chapters from a specific textbook.
2. **Embedding and Storage**: Uses FAISS for vector storage and HuggingFace embeddings.
3. **Retriever**: Implements an ensemble retriever combining BM25 and FAISS.
4. **Router Chain**: Determines whether to use vector store, search engine, or fallback based on the query.
5. **Relevancy Check**: Filters retrieved documents based on relevance to the query.
6. **Generation**: Uses a language model to generate responses based on retrieved context.
7. **LangGraph Workflow**: Orchestrates the entire process using a state graph.

## Setup

1. Install required packages:
   ```
   pip install langchain langchain-community pypdf sentence-transformers tiktoken rank_bm25 langchain-together tavily-python langgraph gradio faiss-gpu
   ```

2. Set up API keys for Together AI and Tavily in your environment variables.

3. Run the notebook cells in order to set up the components and launch the Gradio interface.

## Usage

Once the Gradio interface is launched, you can interact with the chatbot by entering questions related to Computer Science or NLP. The system will retrieve relevant information and generate a response.

## Note

This project is designed for educational purposes and may require adjustments for production use.
