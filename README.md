**DocumentScraperCoLab**

_RAG Document Scraper created through Google CoLab_

DocumentScraperCoLab is a Retrieval-Augmented Generation (RAG) system built to run in Google Colaboratory. 
It enables you to upload documents (such as PDFs, Word files, or text files) and query them using a large language model (LLM), providing accurate, context-aware answers grounded in your documents. 
The repository also includes a comprehensive bank statement verification tool .

**Overview**

A RAG system enhances LLM responses by first retrieving relevant information from your documents and then using that information as context for generation . This approach prevents hallucinations and allows the model to work with private or custom data .

**DocumentScraperCoLab follows a typical RAG pipeline :**

_Document Loading_: Upload and load your document (PDF, DOCX, TXT) .

_Chunking_: Split the text into smaller, manageable chunks .

_Embedding & Indexing_: Generate vector embeddings for each chunk and store them in a vector database .

_Retrieval_: For a user query, find the most semantically similar document chunks .

_Generation_: Use the retrieved chunks as context for an LLM to generate an informed answer .

**Features**

_Document Processing_: Upload and process PDF, DOCX, and TXT files .

_RAG Pipeline_: Fully functional Retrieval-Augmented Generation workflow.

_LLM Integration_: Uses a large language model (e.g., CapybaraHermes-2.5-Mistral-7B-GGUF) for answering questions .

_Vector Database_: Employs Chroma for efficient vector storage and similarity search .

_Bank Statement Verification_: Includes a tool for comprehensive bank statement verification .

_Colab Environment_: Designed to run entirely within a Google Colab notebook, leveraging free GPU resources .

**How It Works**

The system is structured as a series of code blocks in a Jupyter Notebook that you execute sequentially .

1. Setup and Installation
The notebook installs necessary packages, including LangChain for orchestration, Chroma for vector storage, and libraries for document processing and web crawling .

2. Document Loading and Processing
You specify the path to your document. The notebook loads it, extracts text, and splits it into chunks using a RecursiveCharacterTextSplitter .

3. Embedding and Indexing
The system uses an embedding model (e.g., from HuggingFace) to create vector representations of each text chunk. These embeddings are then stored in a Chroma vector store .

4. Querying the LLM (RAG)
You enter a question in the interactive prompt. The system:

Embeds your question.

Retrieves the most relevant chunks from Chroma .

Constructs a prompt with the retrieved context and your question .

Sends the prompt to the LLM (e.g., CapybaraHermes-2.5-Mistral-7B-GGUF) .

Displays the generated answer .

Project Structure
The repository contains:

DocumentScraperCoLab/

├── DocumentScraper/

│   └── [Notebook files]

├── .gitignore

└── README.md

**Getting Started**

**Prerequisites**

A Google account to access Google Colab.

Basic familiarity with running Jupyter notebooks.

Setup

Open the project's Google Colab notebook.

Run the cells sequentially to install dependencies and set up the environment.

Upload your document when prompted.

Start querying your document.

Technologies Used
Google Colab: Cloud-based environment with GPU support .

LangChain: Framework for building LLM applications .

Chroma: Vector database for storing and retrieving embeddings .

HuggingFace: Platform for accessing LLMs and embedding models .

BeautifulSoup & aiohttp: Used for web crawling features .

**Acknowledgments**

Uses LangChain, HuggingFace, and other open-source libraries.
