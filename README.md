# 📚 RAG Documents Question Answering Bot

An AI-powered **Document Question Answering system** built using **Retrieval-Augmented Generation (RAG)**.

This project demonstrates how documents can be processed, converted into embeddings, stored in a vector database, and searched to retrieve relevant information before generating an answer with a Large Language Model (LLM).

---

## 🚀 Features

* 📄 PDF and document loading
* ✂️ Text splitting and chunking
* 🔢 Text embeddings
* 🗄️ ChromaDB vector database
* 🔎 Semantic similarity search
* 📚 Document retrieval
* 🤖 LLM-powered question answering
* 🔗 Retrieval-Augmented Generation (RAG) pipeline

---

## 🧠 What is RAG?

**Retrieval-Augmented Generation (RAG)** combines information retrieval with Large Language Models.

Instead of asking an LLM to answer a question only from its existing knowledge, the system first searches a collection of documents for relevant information. The retrieved content is then provided to the LLM as context for generating the answer.

### RAG Pipeline

```text
                 📄 Documents
                      │
                      ▼
              Document Loading
                      │
                      ▼
               Text Chunking
                      │
                      ▼
                 Embeddings
                      │
                      ▼
                 🗄️ ChromaDB
                      │
                      ▼
                 🔎 Retriever
                      │
                      ▼
              Relevant Chunks
                      │
                      ▼
                    🤖 LLM
                      │
                      ▼
                 💬 Answer
```

---

## 🔄 How It Works

### 1. Document Loading

Documents are loaded and converted into a format that can be processed by the RAG pipeline.

### 2. Text Chunking

Large documents are divided into smaller chunks.

This makes it easier to retrieve only the relevant portions of a document instead of sending the entire document to the LLM.

### 3. Embeddings

Each text chunk is converted into a numerical vector representation called an **embedding**.

Embeddings allow the system to compare the semantic meaning of text.

### 4. Vector Storage

The generated embeddings are stored in **ChromaDB**, which acts as the vector database.

### 5. Similarity Search

When a user asks a question, the question is converted into an embedding and compared with the stored document embeddings.

The most relevant chunks are retrieved.

### 6. Answer Generation

The retrieved document context is provided to the LLM, which generates an answer based on the relevant information.

---

## 🛠️ Technologies Used

| Technology           | Purpose                         |
| -------------------- | ------------------------------- |
| Python               | Core programming language       |
| LangChain            | RAG and document processing     |
| ChromaDB             | Vector database                 |
| Embedding Model      | Semantic representation of text |
| Large Language Model | Answer generation               |
| PyPDF                | PDF document processing         |

---

## 📂 Project Structure

```text
RAG-Documents-Question-Answers-Bot/
│
├── data/
│   └── documents/
│
├── notebook/
│
├── src/
│   └── ...
│
├── requirements.txt
├── pyproject.toml
├── README.md
└── .gitignore
```

> The exact structure may change as the project is further organized into modules.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/wardaabdullah870-gif/RAG-Documents-Question-Answers-Bot.git
```

### 2. Navigate to the project

```bash
cd RAG-Documents-Question-Answers-Bot
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

### 4. Activate the virtual environment

For Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 API Keys

The project uses an external model provider for embeddings and/or answer generation.

Create a `.env` file in the project directory and add the required API key.

Example:

```env
API_KEY=your_api_key_here
```

Use the exact environment variable required by the model provider configured in the project.

Add the following to `.gitignore`:

```text
.env
.venv/
__pycache__/
*.pyc
```

---

## ▶️ Running the RAG Pipeline

Run the main Python script or notebook containing the RAG pipeline.

For example:

```bash
python main.py
```

If the project is being developed through Jupyter Notebook, open the notebook inside the `notebook/` directory and execute the cells in order.

---

## 💬 Example

A user can ask a question such as:

```text
What is the main topic of the document?
```

The system then:

```text
Question
   ↓
Question Embedding
   ↓
Similarity Search
   ↓
Relevant Document Chunks
   ↓
Context + Question
   ↓
LLM
   ↓
Generated Answer
```

---

## 📊 Why Use RAG?

RAG is useful when working with information that may not be part of an LLM's general training knowledge.

Examples include:

* Research papers
* Company documents
* Technical documentation
* Reports
* Books
* Manuals
* Private knowledge bases

Instead of retraining an LLM for every document collection, RAG allows external information to be retrieved and provided to the model at query time.

---

## 🎯 Learning Objectives

This project was created to develop practical experience with:

* Python
* LangChain
* Document loading
* PDF processing
* Text chunking
* Embeddings
* Vector databases
* ChromaDB
* Similarity search
* Retrieval-Augmented Generation
* Large Language Models
* Prompt construction

---

## 🔮 Future Improvements

Planned improvements include:

* 📤 Allow users to upload their own PDF documents
* 📚 Support multiple document collections
* 🔍 Improve retrieval quality
* 🔗 Display the source documents used for each answer
* 🧪 Add retrieval and answer evaluation
* 💬 Add conversational memory
* 🌐 Build a web interface for the RAG system

---

## 👩‍💻 Author

**Warda Abdullah**

Python Developer | AI & RAG Developer

GitHub:
https://github.com/wardaabdullah870-gif

