# 🌾 Kisan RAG Evaluation Suite

## 📌 Overview

**Kisan RAG Evaluation Suite** is an evaluation framework for a Retrieval-Augmented Generation (RAG) system that answers questions related to government schemes and farmer-focused information.

Instead of evaluating the RAG application as a single system, this project separately examines **how well information is retrieved** and **how accurately answers are generated**.

## 🎯 Objectives

* Measure the quality of document retrieval.
* Evaluate the correctness and relevance of generated answers.
* Test the RAG system with **30+ question-answer pairs**.
* Include **unanswerable questions** to test unsupported-answer handling.
* Measure retrieval and generation performance separately.
* Identify common errors and areas for improvement.

## 🔄 Evaluation Workflow

```text
Government Scheme PDF
        ↓
PDF Text Extraction
        ↓
Document Chunking
        ↓
Embedding Generation
        ↓
Vector Search
        ↓
Relevant Context Retrieval
        ↓
Gemini Question Answering
        ↓
Retrieval Evaluation
        ↓
Generation Evaluation
        ↓
Results & Error Analysis
```

## 📚 Evaluation Dataset

The evaluation dataset contains **30+ questions** based on information available in the source document.

The dataset also contains deliberately **unanswerable questions**. These questions help evaluate whether the RAG system correctly avoids producing information that is not supported by the available context.

## 📊 Evaluation Metrics

### 🔎 Retrieval Evaluation

Retrieval quality is evaluated by checking whether the relevant information required to answer a question appears in the retrieved chunks.

### 💬 Generation Evaluation

Generation quality is evaluated by comparing the generated response with the expected answer and checking whether the response is supported by the retrieved context.

## 📈 Results & Analysis

The evaluation results are stored in the project's results table/CSV file.

The analysis focuses on:

* Retrieval accuracy
* Answer accuracy
* Context relevance
* Handling of unanswerable questions
* Retrieval failures
* Generation failures
* Potential improvements

## 🛠️ Technologies

* **Python**
* **Google Colab**
* **Gemini API**
* **RAG**
* **Embeddings**
* **Vector Search**
* **PyPDF**

## 💡 Why This Project?

A RAG system can produce a fluent answer even when the retrieved information is incomplete or irrelevant.

Therefore, this project evaluates the two important stages independently:

> **Did the system retrieve the right information?**

and

> **Did the system generate an answer that is supported by that information?**

This makes the evaluation more measurable and helps identify whether an error originates from **retrieval** or **answer generation**.

## 🚀 Future Improvements

* Expand the evaluation dataset.
* Experiment with different chunk sizes and overlap values.
* Compare multiple embedding models.
* Test different retrieval strategies.
* Add automated semantic evaluation.
* Improve detection of unsupported answers.
* Evaluate across multiple government-scheme documents.
* Add visualization of evaluation results.

## 👤 Author

**Saniya Shaikh**

Computer Science Student
RAG & Generative AI Project

---

⭐ **Built as part of an AgenticX RAG Evaluation task to demonstrate measurable and reproducible evaluation of a RAG-based question-answering system.**
