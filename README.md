# 🚀 Azota Local PRO (Azota Exam Parser with Gemini AI)

An intuitive Python-based web application powered by **Streamlit** and **Google's Gemini API**. It automatically reads, extracts, and converts multiple-choice exam questions from PDF or DOCX files into a highly structured JSON format while providing a visually stunning, interactive quiz interface.

## ✨ Key Features

- **Multi-format File Support:** Seamlessly upload and process exam files in `.pdf` (via PyMuPDF) and `.docx` (via python-docx) formats.
- **Smart AI Extraction:** Leverages the **Gemini Flash** model to analyze raw text and automatically recognize the exam structure, including question numbers, question content, multiple-choice options (A, B, C, D), and the correct answers.
- **Large File Processing & Caching:** Automatically chunks large texts to ensure smooth AI processing without hitting token limits. Parsing results are cached (`.azota_ai_cache`) using SHA-1 file hashing to significantly save API calls on subsequent reloads.
- **Interactive Quiz UI:** A fully custom-styled, modern web interface with **Light/Dark Mode** support. It includes a progress bar, real-time grading, correct/wrong answer reveal, and a question minimap (q-grid) for easy tracking.
- **Structured Data Export:** Easily save and export the parsed question data into a standard JSON format for external use.

## 🛠️ Tech Stack

- **Core Language:** Python 3.x
- **Web Interface:** Streamlit
- **Artificial Intelligence:** Google Generative AI (Gemini Flash API)
- **Document Processing:** `PyMuPDF` (fitz) for PDF, `python-docx` for DOCX
- **Other Libraries:** `json`, `os`, `hashlib`, `re`

## 📦 Getting Started & Local Installation

### 1. Prerequisites
- Python 3.9 or higher

### 2. Install Required Dependencies
Open your terminal or command prompt and run the following command to install the required libraries:
```bash
pip install streamlit PyMuPDF python-docx google-generativeai
```

### 3. Setup API Key
You will need a **Google Gemini API Key**. You can get one for free at [Google AI Studio](https://aistudio.google.com/). 
When you launch the application, the interface will prompt you to enter this API Key in the sidebar.

### 4. Run the Application
Execute the following command in the directory containing the source code:
```bash
streamlit run azota.py OR python -m streamlit run azota.py
```
The application will automatically open in your default web browser at: `http://localhost:8501`.

## 📸 Quick Start Guide

1. Open the application in your browser.
2. Enter your **Gemini API Key** in the settings panel located in the sidebar.
3. Upload your exam file (`.pdf` or `.docx`).
4. Wait for the AI to read and extract the questions. This process features a clear progress indicator, and questions will be cached for lightning-fast reloading next time.
5. Start taking the interactive quiz directly on the web interface, complete with smooth animations and auto-grading logic!

---
*This project is developed for educational purposes, aiming to assist teachers and students in digitizing study materials quickly and intelligently.*
