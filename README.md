# RAG-understanding

A practical repository for learning and understanding **Retrieval-Augmented Generation (RAG)** from the basics.

This repository contains my experiments, notes, notebooks, documents, and code developed while learning how RAG systems work.

---

## What is RAG?

**Retrieval-Augmented Generation (RAG)** is a technique that combines information retrieval with a Large Language Model (LLM).

Instead of relying only on the knowledge stored in an LLM, a RAG system:

1. Takes a user's query
2. Searches a collection of relevant documents
3. Retrieves the most relevant information
4. Provides that information to the LLM
5. Generates an answer based on the retrieved context

### Basic RAG Pipeline

```text
Documents
    ↓
Document Loading
    ↓
Text Splitting / Chunking
    ↓
Embeddings
    ↓
Vector Store
    ↓
User Query
    ↓
Similarity Search
    ↓
Relevant Documents
    ↓
LLM
    ↓
Generated Answer
```

---

## Repository Structure

```text
RAG/
│
├── data/
│   ├── pdf/
│   │   └── PDF documents used for experimentation
│   │
│   ├── text_files/
│   │   └── Text documents used for RAG experiments
│   │
│   └── vector_store/
│       └── Local vector database generated during experiments
│
├── notebook/
│   ├── document.ipynb
│   └── images used in the notebooks
│
│
├── rag_basics.txt
│   └── Notes about fundamental RAG concepts
│
├── requirements.txt
│   └── Python dependencies
│
└── .gitignore
    └── Files and folders excluded from Git
```

---

## Topics Covered

The repository is being developed progressively. The main topics include:

- What is RAG?
- Why RAG is needed
- Document loading
- PDF processing
- Text extraction
- Text chunking
- Embeddings
- Vector databases
- Similarity search
- Retrieval
- Context for LLMs
- RAG pipeline design
- Experimentation with different documents and retrieval methods

---

## Technologies Used

- **Python**
- **Jupyter Notebook**
- **LangChain**
- **ChromaDB**
- **Hugging Face / Embedding Models**
- **Groq API**
- **LLMs**
- **Git & GitHub**

---

## Setup

### 1. Clone the repository

```bash
git clone git@github.com:adityaDev-2005/RAG-understanding.git
cd RAG-understanding
```

You can also clone it using HTTPS:

```bash
git clone https://github.com/adityaDev-2005/RAG-understanding.git
cd RAG-understanding
```

### 2. Create a virtual environment

```bash
python3 -m venv venv
```

Activate it:

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file:

```text
GROQ_API_KEY=your_groq_api_key
```

Do **not** commit the `.env` file to GitHub.

The repository's `.gitignore` is configured to keep environment variables and other local files out of Git.

---

## Learning Approach

This repository follows a step-by-step approach rather than directly building a complex RAG application.

### Phase 1 — Understanding RAG

Learn the basic concepts:

- What RAG is
- Why retrieval is required
- RAG vs. normal LLM generation
- Basic RAG architecture

### Phase 2 — Working with Documents

Experiment with different document types:

- PDF
- TXT
- Other text-based documents

Understand how documents are loaded and converted into usable text.

### Phase 3 — Chunking

Learn how large documents are divided into smaller chunks.

Important concepts:

- Chunk size
- Chunk overlap
- Why chunking affects retrieval quality

### Phase 4 — Embeddings

Learn how text is converted into numerical vectors.

```text
Text
  ↓
Embedding Model
  ↓
Vector
```

These vectors allow semantically similar pieces of text to be compared.

### Phase 5 — Vector Store

Store document embeddings in a vector database and perform similarity searches.

```text
Document Chunks
      ↓
   Embeddings
      ↓
  Vector Store
      ↓
Similarity Search
```

### Phase 6 — Retrieval

Given a user query, retrieve the most relevant document chunks.

```text
User Query
    ↓
Query Embedding
    ↓
Vector Search
    ↓
Relevant Chunks
```

### Phase 7 — Generation

Pass the retrieved context to an LLM to generate an answer.

```text
User Query + Retrieved Context
              ↓
             LLM
              ↓
           Answer
```

### Phase 8 — Building a Complete RAG System

After understanding the individual components, combine them into a complete RAG pipeline.

---

## Example Workflow

A simple RAG system can be represented as:

```text
        Documents
            │
            ▼
     Document Loader
            │
            ▼
       Text Chunks
            │
            ▼
       Embedding Model
            │
            ▼
       Vector Database
            │
            │
User Query ─┘
     │
     ▼
Query Embedding
     │
     ▼
Similarity Search
     │
     ▼
Relevant Context
     │
     ▼
      LLM
     │
     ▼
Generated Answer
```

---

## Notes

The `rag_basics.txt` file contains notes created while learning the fundamental concepts of RAG.

The Jupyter notebooks contain practical experiments and implementation steps.

This repository is intended to document the learning process and gradually evolve into a more complete RAG application.

---

## Future Improvements

Possible future additions include:

- Better document chunking strategies
- Metadata-based filtering
- Improved retrieval methods
- Hybrid search
- Reranking
- Retrieval evaluation
- Better prompt construction
- Conversation history
- Source citations
- A simple web interface
- End-to-end RAG application

---

## Goal

The main goal of this repository is to build a strong understanding of **how RAG systems work internally**, rather than treating RAG as a black-box framework.

The project will gradually move from:

```text
Understanding
     ↓
Experimentation
     ↓
Individual Components
     ↓
Complete RAG Pipeline
     ↓
Practical Application
```

---

## Author

**Aditya Asutosh Mishra**

GitHub: [@adityaDev-2005](https://github.com/adityaDev-2005)

---

## License

This project is primarily intended for learning and experimentation.
:::

One small recommendation: because this README currently describes `data/vector_store/` as part of the repository, **if you later remove that generated vector store from Git and add it to `.gitignore`, we should update this README accordingly**.
