<h1 align="center">🚀 Honeypot Scam Detection System V9</h1>

<p align="center">
AI-powered conversational honeypot that detects scams, engages attackers, and extracts prosecution-ready intelligence in real time.
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Flask](https://img.shields.io/badge/Flask-API-lightgrey)
![AI Powered](https://img.shields.io/badge/AI-Multi--LLM-purple)
![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)
![Security](https://img.shields.io/badge/Focus-Cybersecurity-red)

</p>

---

## 🧾 Description

This system simulates a realistic human victim in scam conversations and covertly gathers criminal intelligence.

Instead of simply detecting scams, the honeypot:

- Detects scam intent using cumulative behavior markers
- Engages scammers using adaptive psychological prompts
- Extracts actionable intelligence (phones, UPI IDs, bank accounts, links)
- Profiles attacker behavior
- Scores intelligence for prosecution readiness
- Sends structured intelligence to an external reporting system

The approach combines rule-based detection + multi-LLM reasoning + behavioral strategy.

---

## 🧠 Approach

### 🔍 Scam Detection Strategy

The system uses **25 cumulative scam markers** across:

- account threats
- urgency pressure
- credential phishing
- KYC fraud
- authority impersonation
- UPI scams
- legal threats
- lottery/refund scams
- social engineering

Markers accumulate across the conversation.  
Once the threshold is crossed → scam flag becomes permanent.

Supports English, Hindi, and Hinglish.

---

### 🕵 Intelligence Extraction Strategy

Every message is scanned for structured entities:

- phone numbers
- bank accounts
- UPI IDs
- phishing domains
- emails
- money amounts

The system includes obfuscation decoding:

```
"Nine eight six five..." → 9865...
```

Intelligence is stored cumulatively per session.

---

### 🎭 Engagement Strategy

The AI operates in dual modes:

| Mode | Behavior |
|------|---------|
| Normal Mode | Casual natural conversation |
| Scam Mode | Strategic intelligence extraction |

Scam mode uses psychological nudging to:

- keep the scammer talking
- request contact details naturally
- avoid raising suspicion
- vary speech patterns

This maximizes intelligence yield while preserving realism.

---

## 🧰 Tech Stack

### Language / Framework
- Python
- Flask API

### Key Libraries
- openai
- google-generativeai
- groq
- requests
- regex
- threading

### LLM / AI Models Used
- OpenAI GPT-4.1-mini
- OpenAI GPT-4o-mini
- Gemini 2.5 Flash Lite
- Gemini 2.5 Flash
- Groq Llama 3.3 70B

Automatic tiered fallback + key rotation included.

---

## ⚙ Setup Instructions

1. Clone the repository

```bash
git clone https://github.com/your-repo/honeypot
cd honeypot
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Set environment variables

```
CHAT_API_KEY=
GEMINI_API_KEY_1=
GEMINI_API_KEY_2=
GROQ_API_KEY_1=
GROQ_API_KEY_2=
API_SECRET_KEY=
GUVI_CALLBACK_URL=
PORT=5000
```

4. Run the application

```bash
python app.py
```

Server starts at:

```
http://localhost:5000
```

---

## 📡 API Endpoint

**URL:** `https://guvi-honeypot-zdg5.onrender.com/honeypot`  
**Method:** POST  
**Authentication:** `honeypot_secret_2026` header

Example request:

```json
{
  "sessionId": "abc123",
  "message": "Your account will be blocked!"
}
```

Example response:

```json
{
  "status": "success",
  "reply": "Arre kya hua?",
  "shouldEndConversation": false
}
```

---

## 🏗 Architecture Overview

```
        User Message
             │
             ▼
      Scam Detection Engine
             │
             ▼
     Multi-Provider LLM Brain
             │
             ▼
    Intelligence Extraction Layer
             │
             ▼
     Profiling + Scoring System
             │
             ▼
      External Callback Reporter
```

---

## 📊 Intelligence Scoring

Sessions are graded:

| Grade | Meaning |
|------|--------|
| 🟣 S | Exceptional intelligence |
| 🔵 A | Prosecution-ready |
| 🟢 B | Strong evidence |
| 🟡 C | Partial intel |
| 🔴 D | Minimal value |

System flags whether intelligence can:

✔ freeze accounts  
✔ block UPI  
✔ track phones  
✔ takedown phishing  

---

## ☁ Deployment

Works on:

- Render

Uses `$PORT` automatically.

---

## 📦 Use Cases

- Scam intelligence gathering
- Cybercrime research
- Security labs
- Law enforcement simulation
- AI honeypot experimentation

---

## ⚠ Disclaimer

For ethical cybersecurity research only.  
Do not deploy outside legal environments.

---

<p align="center">
⭐ Star this project if you found it interesting
</p>

