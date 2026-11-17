# Agentic RAG Research Assistant

An AI-powered research assistant designed to retrieve, analyse and synthesise information from multiple knowledge sources, including PDF documents and web pages. Built using Python, Google's Gemini models, Agno and ChromaDB, the system combines semantic retrieval, web search and LLM-based reasoning to generate context-aware responses.

## Key Features

- **Multi-Source Document Ingestion:** Processes PDF documents and web URLs to create a unified knowledge base for information retrieval.
- **LLM-Powered Reasoning:** Integrates Google's Gemini models to analyse retrieved information and generate context-aware responses.
- **Query Rewriting:** Incorporates an AI-driven query rewriting approach to improve question formulation and information retrieval.
- **Web Search Integration:** Uses Exa AI to retrieve relevant external information and supplement document-based research.
- **Semantic Search:** Utilises ChromaDB and Google Gemini embeddings to enable vector-based document retrieval.
- **Context-Aware Responses:** Combines retrieved document context and external information to generate relevant answers.
- **Interactive Interface:** Provides a Streamlit-based interface for document uploads, URL inputs and conversational queries.

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| LLM | Google Gemini 2.0 Flash Thinking (experimental model) |
| Agent Framework | Agno |
| Document Processing | LangChain Community |
| Web Search | Exa AI |
| Embeddings | Google Gemini Embeddings |
| Vector Database | ChromaDB |
| User Interface | Streamlit |
| HTML Parsing | BeautifulSoup |

## System Architecture

The application follows a retrieval-augmented generation workflow:

1. **Input Processing:** Accepts PDF documents and web URLs as information sources.
2. **Document Ingestion:** Extracts and processes textual content from uploaded documents and web pages.
3. **Embedding Generation:** Converts processed content into vector representations using Gemini embeddings.
4. **Vector Storage:** Stores document embeddings in ChromaDB for semantic retrieval.
5. **Query Processing:** Uses an AI-driven query rewriting approach to improve retrieval queries.
6. **Information Retrieval:** Retrieves relevant document context and supplements it with external web search through Exa AI.
7. **Response Generation:** Uses Gemini to synthesise retrieved information into context-aware responses.

## Core Workflow

| Stage | Component | Function |
|---|---|---|
| Ingestion | PyPDFLoader / WebBaseLoader | Extracts information from PDFs and web pages |
| Embedding | Gemini Embeddings | Converts document content into vector representations |
| Storage | ChromaDB | Maintains vector-based document storage |
| Query Processing | Query Rewriter Agent | Reformulates queries for improved retrieval |
| Web Research | Exa AI Tools | Retrieves relevant external information |
| Reasoning | Gemini Agent | Generates responses using retrieved context |
| Interface | Streamlit | Provides an interactive research experience |

## Installation & Setup

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd agentic-rag-research-assistant
```

### 2. Install Dependencies

```bash
pip install streamlit agno google-generativeai langchain-community beautifulsoup4 chromadb hnswlib
```

### 3. Configure API Credentials

Obtain the required API keys:

- [Google AI Studio](https://aistudio.google.com/) – Gemini API.
- [Exa AI](https://dashboard.exa.ai/) – Web search API.

Configure credentials through environment variables or a local secrets configuration. Never commit API keys to the repository.

### 4. Run the Application

```bash
streamlit run agentic_rag.py
```

## Potential Applications

- Research and knowledge discovery across multiple documents.
- Question answering over technical reports and research papers.
- Combining internal document knowledge with external web information.
- Information extraction and research assistance.
- Context-aware analysis of unstructured information.

## Future Enhancements

- Improved source-level citations and document references.
- Advanced retrieval optimisation and query routing.
- Retrieval quality and answer faithfulness evaluation.
- Support for additional document formats.
- Improved error handling and retrieval validation.
- Enhanced document management and user experience.

## Credits & Acknowledgements

This project builds upon the open-source work by **Simranjeet Singh**, available in the original [Awsome_AI_Agents repository](https://github.com/simranjeet97/Awsome_AI_Agents/tree/main/GenAI_AgenticRAG_PDF_WebSearch).

The original implementation is acknowledged as the foundation for further learning, exploration and development.
