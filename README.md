# 🚀 Advanced RAG Search Engine (Keyword + Semantic + Multimodal)

A production-style **Retrieval-Augmented Generation (RAG)** system built from scratch in Python — combining **keyword search, semantic search, hybrid ranking, and multimodal retrieval** into a unified CLI.

This project goes beyond basic RAG by implementing **core search engine internals + modern LLM workflows**.

---

## 🔥 Features

### 🔎 Search Systems

* ✅ Keyword Search (TF, TF-IDF, BM25)
* ✅ Semantic Search (vector embeddings)
* ✅ Hybrid Search:

  * Weighted scoring (BM25 + semantic)
  * Reciprocal Rank Fusion (RRF)
* ✅ Re-ranking (cross-encoder, batch, individual)

---

### 🧠 Retrieval-Augmented Generation (RAG)

* ✅ Search + grounded answer generation
* ✅ Multi-document summarization
* ✅ Question answering
* ✅ Answer generation with citations

---

### 🖼️ Multimodal Search

* ✅ Image → embedding → search
* ✅ Image + text → query rewriting (Gemini)
* ✅ Cross-modal retrieval (image ↔ text)

---

### ⚙️ Search Engineering

* ✅ Inverted Index (fast retrieval)
* ✅ Tokenization, stopwords, stemming
* ✅ Chunking strategies:

  * Fixed-size chunks
  * Semantic chunking (sentence-aware)

---

### 📊 Evaluation

* ✅ Precision@k, Recall@k, F1-score
* ✅ LLM-based relevance judging

---

## 🏗️ CLI Commands

### 🔑 Keyword Search

```bash
python cli.py build
python cli.py search "alien movie"

python cli.py tf <doc_id> <term>
python cli.py idf <term>
python cli.py tfidf <doc_id> <term>

python cli.py bm25search "space sci-fi"
```

---

### 🧠 Semantic Search

```bash
python cli.py verify
python cli.py embed_text "hello world"
python cli.py search "space exploration"

python cli.py chunk "long text" --chunk-size 200
python cli.py semantic_chunk "text"
python cli.py search_chunked "query"
```

---

### 🔀 Hybrid Search

```bash
python cli.py weighted-search "query" --alpha 0.7
python cli.py rrf-search "query" --k 60 --rerank-method cross_encoder
```

---

### 🤖 RAG (LLM-powered)

```bash
python cli.py rag "What is the plot of Interstellar?"
python cli.py summarize "space movies"
python cli.py citations "AI in movies"
python cli.py question "What is Inception about?"
```

---

### 🖼️ Multimodal Search

```bash
python cli.py image_search path/to/image.jpg
python cli.py verify_image_embedding path/to/image.jpg
```

---

### 🧪 Evaluation

```bash
python cli.py --limit 5
```

---

## 🧠 Architecture Overview

```
User Query / Image
        ↓
   Query Processing
        ↓
 ┌───────────────┐
 │ Retrieval     │
 │  - Keyword    │
 │  - Semantic   │
 │  - Hybrid     │
 └───────────────┘
        ↓
   Re-ranking
        ↓
 Retrieved Context
        ↓
      LLM
        ↓
 Final Answer
```

---

## 🧰 Tech Stack

* **Python**
* **NLTK** (text processing)
* **Vector Embeddings**
* **BM25 / TF-IDF**
* **Gemini API** (LLM + multimodal)
* **dotenv** (env management)

---

## ⚙️ Setup

```bash
git clone <your-repo>
cd <your-repo>

python -m venv venv
source venv/bin/activate

pip install -r requirements.txt
```

### 🔑 Environment Variables

```bash
GEMINI_API_KEY=your_api_key_here
```

---

## 📌 Key Learnings

* How real-world **search engines** work internally
* Difference between **keyword vs semantic vs hybrid search**
* How to build **RAG systems without relying on frameworks**
* Importance of **retrieval quality in LLM outputs**
* Handling **multimodal inputs (image + text)**

---

## 🚧 Future Improvements

* [ ] UI / Web interface
* [ ] Streaming LLM responses
* [ ] Better ranking models
* [ ] Distributed indexing
* [ ] Real-world dataset integration

---

## ⭐ Why This Project Stands Out

Most RAG projects:

> Glue APIs together

This project:

> Builds the **entire search + retrieval + ranking + generation pipeline from scratch**

---

## 🤝 Contributing

Pull requests and experiments are welcome — especially around:

* Ranking improvements
* Faster retrieval
* Better embeddings

---
