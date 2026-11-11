# 📄 Papertrail — Chat with your PDF

> **Paper leaves traces. Now you can read them.**
> Drop in a document and Papertrail cuts it into small, page-aware pieces your AI can search, so every answer can point back to the exact page it came from.

### 🔗 Live Demo: [https://paper-trail-rust.vercel.app](https://paper-trail-rust.vercel.app/)

---

## ✨ Overview

Papertrail is the ingestion foundation of a **citation-first RAG (Retrieval-Augmented Generation)** pipeline. It takes a PDF, extracts its text page by page, and slices it into overlapping, page-tagged chunks that are ready for embedding and retrieval.

Most "chat with your PDF" tools hide the chunking step and lose track of where an answer came from. Papertrail makes that step visible, controllable and traceable: you see exactly how your document is cut, and every chunk remembers its page.

---

## 🚀 Features

- **📥 Drag-and-drop PDF upload**: drop a file or tap to choose one.
- **🔒 Runs entirely in your browser**: your PDF never leaves your device.
- **📃 Page-by-page text extraction**: text is read per page, with page numbers kept as metadata.
- **📊 Live document stats**: file name, page count, word count and approximate token count.
- **✂️ Adjustable chunking**: set your own **chunk size** (default 500 tokens) and **overlap** (default 100 tokens).
- **🧭 Document timeline**: a visual map where each dashed cut marks the end of a chunk and numbers mark page starts.
- **🔍 Expand all pages**: inspect the raw extracted text for every page.
- **💾 JSON export**: download both the **extracted pages JSON** and the **chunks JSON**, ready for embeddings.

---

## 🧠 How it works

| Step | Stage | What happens |
|------|-------|--------------|
| 01 | **Upload** | Choose a PDF. It never leaves your device. |
| 02 | **Extract** | Text is read page by page, with page numbers as metadata. |
| 03 | **Cut** | Pages are sliced into overlapping chunks you can size yourself. |
| 04 | **Embed** | *Coming next:* turn each chunk into a vector. |
| 05 | **Ask** | *Coming next:* retrieve, answer and cite pages. |

The roadmap continues towards embeddings, a vector store, retrieval and chat.

---

## 🌟 What makes Papertrail unique

1. **Page-aware chunks.** Every chunk keeps its source page numbers, so future answers can cite *"Page 12"*, *"Clause 4.2"* or *"Table 3"* instead of vaguely pointing at a file.
2. **Privacy by design.** All parsing and chunking happen client-side. No upload, no server, no account.
3. **Transparent chunking.** Most tools hide how text is split. Papertrail lets you tune chunk size and overlap and see the result on a visual timeline.
4. **Overlapping chunks.** Overlap preserves context across chunk boundaries, which improves retrieval quality.
5. **Embedding-ready output.** Clean JSON exports drop straight into any embedding model or vector database.
6. **A distinctive, editorial interface.** A calm, paper-inspired design that makes a technical pipeline easy to understand.

---

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS, JavaScript
- **PDF parsing:** client-side text extraction (PDF.js-style, in the browser)
- **Hosting:** [Vercel](https://vercel.com)

> Update this list if your implementation differs.

---

## 📦 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<your-repo>.git

# 2. Open the project
cd <your-repo>

# 3. Run it locally (any static server works)
npx serve .
```

Then open the local URL, drop in a PDF and start cutting.

---

## 🗺️ Roadmap

- [x] PDF upload and page-by-page extraction
- [x] Adjustable overlapping chunks
- [x] Document timeline visualisation
- [x] JSON export for extracted text and chunks
- [ ] Generate embeddings for each chunk
- [ ] Vector store
- [ ] Retrieval
- [ ] Chat with page-level citations

---

## 👤 Author

**Vishnu Prasath S**
[GitHub](https://github.com/vishnuprasath2406) · [LinkedIn](https://linkedin.com/in/Vishnu2406)

---

⭐ If you find this project useful, consider giving it a star!
