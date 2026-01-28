📰 AI-Powered Fake News & Statement Verification System
📌 Project Overview

This project is an AI-driven web application designed to verify the factual correctness of user-provided statements. It intelligently combines Large Language Models (LLMs) with real-time news data to classify statements as REAL, FAKE, PARTIAL REAL, or PARTIAL FAKE, along with a deterministic confidence score.

The system is built to reduce hallucinations by validating claims against live external sources, making it suitable for misinformation detection, content moderation, and fact-checking use cases.

🚀 Key Features

✅ Verifies factual statements using multi-source AI reasoning

🧠 Integrates OpenAI (ChatGPT) and Google Gemini

🌐 Uses SerpAPI for real-time news validation

🧩 Handles multiple statements in a single input

📊 Provides consistent confidence scores for the same input

🖥️ Simple and interactive Flask-based web interface

🔁 Reproducible results using deterministic hashing

🛠️ Tech Stack

Backend: Python, Flask

Frontend: HTML, CSS

AI Models & APIs:

OpenAI (ChatGPT – structured JSON responses)

Google Gemini (entity/person-based explanations)

SerpAPI (live Google News search)

Other: REST APIs, SHA-256 hashing, semantic analysis

📂 Project Structure
├── app.py                 # Flask application entry point
├── final9.py              # Core AI verification logic
├── templates/
│   └── index.html         # Web UI
├── static/
│   └── style.css          # Styling
├── __pycache__/           # Compiled Python files

⚙️ How the System Works
1️⃣ User Input Processing

Accepts single or multiple statements

Supports comma-separated or line-separated inputs

2️⃣ Intelligent Statement Routing

Person names detected → Verified using Google Gemini

General claims detected → Verified using:

SerpAPI (news headlines)

ChatGPT (structured factual explanation)

3️⃣ Multi-Source Verification

Combines LLM reasoning with real-world evidence

Minimizes hallucination by grounding responses in live data

4️⃣ Semantic Consistency Check

Detects contradictions or negations in explanations

Labels each statement as REAL or FAKE

5️⃣ Aggregated Final Classification

REAL

FAKE

PARTIAL REAL

PARTIAL FAKE

6️⃣ Deterministic Confidence Scoring

Uses SHA-256 hashing

Same input → same confidence score

Ensures reproducibility and evaluation consistency

📤 Output Format

The system returns:

Final Result: PARTIAL REAL
Confidence Score: 0.72
Explanation: <Detailed factual explanations for each statement>

🔐 Environment Variables Required

Before running the project, set the following API keys:

export OPENAI_API_KEY="your_openai_api_key"
export GEMINI_API_KEY="your_gemini_api_key"
export SERPAPI_API_KEY="your_serpapi_key"

▶️ How to Run the Application
1️⃣ Install Dependencies
pip install flask openai google-generativeai requests

2️⃣ Run the Flask App
python app.py

3️⃣ Open Browser

The application automatically opens at:

http://127.0.0.1:5000/

🧪 Example Use Cases

Fake news detection

Social media content verification

Academic fact-checking tools

AI-assisted journalism

Misinformation monitoring systems

📈 Future Enhancements

Confidence calibration using ground-truth datasets

Source credibility weighting

Multilingual fact verification

Database-backed verification history

Visualization dashboard for fact-checking results

👨‍💻 Author

Manoj M J
Data Science & AI Enthusiast

⭐ Acknowledgements

OpenAI

Google Gemini

SerpAPI
