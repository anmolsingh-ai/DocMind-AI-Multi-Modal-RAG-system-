# DocMind-AI-Multi-Modal-RAG-system-


# 🧠 DocMind – Multi-Modal Retrieval-Augmented Generation System

> An AI system that reads, sees, understands, and answers from complex PDFs including text, tables, and images.

---

## 🚀 What is DocMind?

**DocMind** is a **Multi-Modal RAG (Retrieval-Augmented Generation)** pipeline that allows users to chat with PDFs containing:

- 📄 Text  
- 📊 Tables  
- 🖼 Images (diagrams, charts, figures)  

It uses **Gemini Vision models + vector search** to produce **accurate, context-aware answers** — even when information is stored in tables or images.

This system goes far beyond standard text-based RAG.

---

## 🔥 Why DocMind is Different

| Traditional RAG | DocMind |
|-----------------|-----------|
| Only text chunks | Text + tables + images |
| Loses visual data | Understands diagrams & charts |
| Weak on PDFs | Designed for PDFs |
| Hallucination prone | AI-generated searchable summaries |

DocMind builds **AI-enhanced embeddings** by understanding every modality before indexing.

---

## 🧩 System Architecture

PDF
└── Unstructured Loader
├── Text
├── Tables
└── Images
↓
Gemini Vision + LLM
↓
AI-Enhanced Chunk Summaries
↓
Vector Embeddings
↓
Chroma Vector Store
↓
Conversational RAG Chain
↓
Chat with Memory




---

## 🛠️ Tech Stack

| Component | Technology |
|--------|------------|
| LLM | Google Gemini 2.5 Flash |
| Vision | Gemini Vision |
| PDF Parsing | Unstructured |
| Chunking | Title-based chunking |
| Embeddings | Gemini Embeddings |
| Vector DB | Chroma |
| RAG | LangChain |
| Memory | ConversationBufferMemory |

---

## 🧠 What Happens Inside

### Step 1 – PDF Ingestion
The PDF is parsed using **Unstructured** to extract:
- Text blocks  
- Tables (HTML)  
- Images (Base64)

---

### Step 2 – Intelligent Chunking
Content is chunked by:
- Titles  
- Semantic boundaries  
ensuring logical sections stay together.

---

### Step 3 – AI-Enhanced Summaries
Each chunk is passed through **Gemini Vision** to generate:

- Searchable descriptions  
- Extracted facts  
- Visual understanding of charts & diagrams  
- Alternative user search phrases  

This dramatically improves retrieval accuracy.

---

### Step 4 – Vector Storage
Chunks are embedded using **Gemini Embeddings** and stored in **Chroma DB**.

---

### Step 5 – Conversational RAG
A LangChain **ConversationalRetrievalChain** enables:

- Multi-turn chat  
- Memory-based follow-ups  
- Source-aware answers  

---

## 💬 Example Queries

```text
Q1: What is the per-layer complexity of self-attention?
Q2: And why is it important?
