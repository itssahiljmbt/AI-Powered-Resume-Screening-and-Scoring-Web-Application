# AI-Powered Resume Analyzer & ATS Scoring System

An **AI-enabled resume screening and analysis web application** built using **Flask (Python)** that evaluates resumes against job descriptions. The system provides **ATS-style keyword matching scores**, **missing skill analysis**, and **AI-driven insights** such as resume summaries, strengths, weaknesses, interview questions, and improvement suggestions using **Google Gemini AI**.

---

## 🚀 Features

### ✅ Resume Parsing

* Supports **`.txt`**, **`.pdf`**, and **`.docx`** resume formats
* Extracts raw text from uploaded resumes
* Handles text-based documents efficiently

### ✅ ATS Keyword Matching

* Extracts relevant keywords from:

  * Job Description
  * Resume content
* Calculates a **matching score (0–100%)**
* Displays:

  * ✅ Matched keywords
  * ❌ Missing keywords

### ✅ AI Resume Analysis (Gemini AI)

* Generates a **concise resume summary**
* Identifies **key strengths**
* Highlights **areas of improvement**
* Output returned in structured **JSON format**

### ✅ AI Interview Question Generator

* Generates **5–7 tailored interview questions**
* Covers:

  * Technical skills
  * Behavioral scenarios
  * Role-specific situations

### ✅ Resume Improvement Suggestions

* Provides **actionable resume enhancement tips**
* Focuses on:

  * Missing keywords
  * Content alignment
  * Presentation quality

---

## 🛠️ Tech Stack

| Component          | Technology              |
| ------------------ | ----------------------- |
| Backend            | Flask (Python)          |
| Resume Parsing     | PyPDF2, python-docx     |
| AI Model           | Google Gemini 2.0 Flash |
| API Communication  | Requests                |
| Frontend           | HTML (Flask Templates)  |
| Keyword Extraction | Regex-based NLP         |

---

## 📁 Project Structure

```
├── app.py
├── templates/
│   └── index.html
├── static/
│   └── (CSS/JS if any)
├── requirements.txt
└── README.md
```

---

## 🔧 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2️⃣ Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install flask requests PyPDF2 python-docx
```

### 4️⃣ Add Google Gemini API Key

Replace the placeholder in `app.py`:

```python
GOOGLE_API_KEY = "YOUR_GOOGLE_GEMINI_API_KEY"
```

> ⚠️ **Security Note:**
> Do NOT expose your API key in public repositories. Use environment variables in production.

---

## ▶️ Running the Application

```bash
python app.py
```

The server will start at:

```
http://127.0.0.1:5000/
```

---

## 📡 API Endpoints

### 🔹 Upload Resume

**POST** `/upload_resume`

**Form Data**

* `resume_file`: `.txt / .pdf / .docx`

**Response**

```json
{
  "extracted_text": "Resume content here"
}
```

---

### 🔹 ATS Resume Scoring

**POST** `/score_resume`

```json
{
  "job_description": "JD text",
  "resume_text": "Resume text"
}
```

**Response**

```json
{
  "score": 78.5,
  "matched_keywords": ["python", "flask"],
  "missing_keywords": ["docker", "aws"]
}
```

---

### 🔹 AI Resume Analysis

**POST** `/analyze_resume_ai`

**Response**

```json
{
  "summary": "Candidate has strong backend experience...",
  "strengths": ["Python expertise", "API development"],
  "weaknesses": ["Limited cloud exposure"]
}
```

---

### 🔹 Interview Question Generator

**POST** `/generate_interview_questions`

**Response**

```json
{
  "questions": [
    "Explain your experience with Flask.",
    "How do you handle API security?"
  ]
}
```

---

### 🔹 Resume Improvement Suggestions

**POST** `/suggest_resume_improvements`

**Response**

```json
{
  "suggestions": [
    "Add cloud-related projects.",
    "Include more quantified achievements."
  ]
}
```

---

## 🎯 Use Cases

* ATS resume screening systems
* HR tech platforms
* College placement portals
* Resume evaluation tools
* Interview preparation platforms

---

## ⚠️ Limitations

* Keyword extraction is regex-based (not deep NLP)
* Works best with text-based PDFs
* AI features require an active Gemini API key

---

## 🔮 Future Enhancements

* Semantic keyword matching using NLP models
* Resume ranking across multiple candidates
* Role-based scoring weightage
* User authentication & dashboard
* Cloud deployment (Docker + AWS/GCP)

---

## 👨‍💻 Author

**Sahil Rathor**
Computer Science Engineer | AI & Web Developer
Specialized in Resume Screening Systems, NLP & AI Integration


Just tell me 👍

