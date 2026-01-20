# 🎓 University AI FAQ Assistant

A smart **AI Chatbot** designed to act as an automated support assistant for university students.

This project utilizes **RAG (Retrieval-Augmented Generation)** technology to answer questions based *strictly* on provided internal documents (e.g., student rulebooks, course syllabi, schedules). It leverages **LangChain** for orchestration, **ChromaDB** for vector storage, and **Groq (Llama 3)** for high-speed inference.

## 🚀 Features

* **📄 PDF Document Analysis:** Automatically loads and processes multiple PDF files from a local directory.
* **🧠 RAG Architecture:** Uses `sentence-transformers` to create embeddings and `ChromaDB` to perform semantic searches, ensuring the bot answers based on facts, not hallucinations.
* **⚡ High-Performance LLM:** Integrated with **Groq API** running the `llama-3.3-70b-versatile` model for lightning-fast responses.
* **🔍 Source Citation:** Every answer includes the specific filename of the document where the information was found.
* **💬 Interactive CLI:** Simple terminal-based interface for continuous conversation.

## 📦 Installation & Setup

### Prerequisites
* Python 3.8 or higher
* A Groq Cloud API Key (Get it [here](https://console.groq.com/))

### Step 1: Clone the Repository
```bash
git clone https://github.com/canonee/AI-University-FAQ-Assistant.git
cd AI-University-FAQ-Assistant
```

### Step 2: Create a Virtual Environment (optional but recommended)
```bash
python -m venv venv
venv\Scripts\activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure Variables
* Create a file named .env in the root directory.
* Add your Groq API key to it:
```bash
GROK_API_KEY=your_actual_api_key_here
```

### Step 5: Prepare Knowledge Base
* Place your PDF files inside `docs` folder. The AI will learn from these files

### Step 6: Run the App
```bash
python Smart_Assistant_FAQ.py
```

## 📂 Project Structure

```bash
AI-University-FAQ-Assistant/
├── docs/                   # Directory where you put your PDF files
├── .env                    # Configuration file for API Keys
├── requirements.txt        # Python dependencies
├── Smart_Assistant_FAQ.py  # Main application logic
└── README.md               # Project documentation
```

## ℹ️ Information
* Uses `HuggingFaceEmbeddings` to accurate vector representations.
* Uses `Chroma` Vector Store.
* Uses the endpoint from *Groq* to run Llama 3.
