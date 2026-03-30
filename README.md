# feature-pdf-rag-chatbot

DF Q&A chatbot using LangChain RAG pipeline

Implements a full Retrieval-Augmented Generation (RAG) pipeline that
allows users to upload any PDF and query its contents using natural
language via an OpenAI LLM.

- Upload and parse PDF files using PyPDFLoader (pypdf)
- Chunk documents into 1000-char segments with 100-char overlap
  using RecursiveCharacterTextSplitter
- Generate semantic embeddings via OpenAIEmbeddings
- Index and store vectors in a FAISS in-memory vector store
- Build a RetrievalQA chain combining the retriever and ChatOpenAI LLM
- Support natural language queries against any uploaded PDF

Dependencies: langchain==0.1.16, langchain-community==0.0.36,
langchain-openai==0.1.7, faiss-cpu, pypdf
