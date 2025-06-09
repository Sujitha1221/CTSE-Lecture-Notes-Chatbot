
# 📘 README: CTSE Lecture Notes Chatbot 

## 📌 Project Title
**CTSE Lecture-Based Question Answering Chatbot using RAG and LLM**

## 📁 Description
This project implements a chatbot that answers questions based on CTSE (Current Trends in Software Engineering) lecture materials. It uses a **Retrieval-Augmented Generation (RAG)** approach that combines semantic search with a transformer-based large language model (`flan-t5-large`) to deliver accurate, context-aware responses.

## 🎯 Features
- ✅ Answers questions using course lecture notes (PDFs and PPTX)
- ✅ Supports both **free-text** and **multiple-choice** queries
- ✅ Uses **semantic similarity** for context retrieval (FAISS)
- ✅ Dynamic prompt trimming to handle token limits (≤512)
- ✅ **Gradio Web UI** for interactive chatbot experience
- ✅ Entirely built and tested in **Google Colab (Jupyter Notebook)**

## 🧱 Technologies & Libraries
| Component | Tool/Library |
|----------|---------------|
| LLM | `flan-t5-large` (Hugging Face Transformers) |
| Embeddings | `all-MiniLM-L6-v2` (`sentence-transformers`) |
| Vector Search | `FAISS` |
| Text Extraction | `PyMuPDF` (PDF), `python-pptx` (PPTX) |
| Interface | Google Colab (CLI) + Gradio (optional) |

## 📂 Lecture Slides
You can access the lecture slides used by the chatbot from the following Google Drive folder:

🔗 [CTSE Lecture Slides (Google Drive)](https://drive.google.com/drive/folders/1gFCfNYB1UnYDLGsE9Dg35Y94ZakXpjVO?usp=sharing)


## 🛠️ Setup Instructions (Google Colab)
1. **Mount Google Drive** and place lecture files under:
   ```
   /content/drive/My Drive/CTSE Assignment-2/lecture slides/
   ```

2. **Install required libraries:**
   ```python
   !pip install python-pptx pymupdf faiss-cpu sentence-transformers transformers gradio
   ```

3. **Run cells in order:**
   - Extract and clean text from lecture slides
   - Split text into chunks
   - Embed chunks and index with FAISS
   - Load `flan-t5-large`
   - Interact using `request_chatbot()` or `gr.Interface()`

## 🧪 Example Questions
**Free-Text:**
- What is DevOps?
- What is the purpose of Docker Compose?
- What is Continuous Deployment?

**MCQ:**
```
What is the primary goal of Continuous Integration?
A. To deploy every change immediately
B. To scale infrastructure
C. To regularly merge and test code changes
D. To replace developers
```
