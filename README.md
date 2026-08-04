# 🤖 Multi-Intent AI Assistant

A **stateful conversational AI assistant** built using **n8n, Docker, and Ollama** that can authenticate users, handle multiple requests in a single conversation, maintain session memory, perform live currency conversion, and answer natural language date & time queries.

> Built entirely using **free and open-source technologies** with **zero API cost**.

---

## 🚀 Features

- 🔐 User Authentication with User ID & PIN
- 🧠 Persistent Session Memory
- 💬 Multi-Intent Conversation Handling
- ✅ Intent Confirmation (Add / Remove / Confirm)
- 💱 Live Currency Conversion using Frankfurter API
- 📅 Natural Language Date & Time Queries
- 🔄 Follow-up Intent Support
- ⚡ Stateful Workflow Architecture
- 🐳 Docker-based Deployment
- 💰 100% Free & Self Hosted

---

## 🏗️ Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| Ollama | Local LLM Runtime |
| Llama 3.1 | Language Model |
| Docker | Containerization |
| Frankfurter API | Live Currency Exchange Rates |
| JavaScript | Workflow Logic |
| Data Tables (n8n) | Session Storage |
| ngrok | Public Access (Demo) |

---

## 📂 Project Structure

```
├── Workflow
│   └── n8n Workflow
│
├── Documentation
│   └── Project Report
│
├── Images
│   └── Workflow Architecture
│
└── README.md
```

---

## 🧠 How It Works

The assistant follows a **State Machine Architecture**.

```
Start
   │
   ▼
Authentication
   │
   ▼
Intent Capture
   │
   ▼
Intent Confirmation
   │
   ▼
Intent Processing
   │
   ▼
Wrap Up
   │
   ▼
End / Continue
```

The assistant stores every conversation state so it remembers:

- Authentication Status
- User Information
- Pending Intents
- Conversation Stage
- Previous Responses

---

## 💱 Supported Functionalities

### Authentication

- User ID + PIN verification
- Three-attempt lockout
- Session persistence

### Currency Conversion

Supports:

- Live Exchange Rates
- Historical Rates
- Yesterday's Rates
- Specific Date Queries

Example:

```
USD to INR today
EUR to GBP yesterday
USD to INR in 2012
```

---

### Date & Time Queries

Examples:

```
Tomorrow
Coming Monday
Next Friday
2 hours from now
3 days later
```

---

### Multi Intent Handling

Example:

```
Convert USD to INR for yesterday
and tell me the date of next Monday.
```

The assistant:

- Detects both requests
- Confirms them
- Lets the user edit/remove intents
- Processes each sequentially

---

## 🔄 Workflow Architecture

The workflow consists of multiple nodes including:

- Chat Trigger
- Session Loader
- State Builder
- Stage Router
- Authentication
- Intent Extractor
- Intent Confirmation
- Currency Processor
- Date Processor
- Wrap-up Agent
- Session Saver

---

## 📊 Evaluation

The project successfully passed all required evaluation scenarios including:

- ✅ Happy Flow
- ✅ Multi-Intent Processing
- ✅ Follow-up Intents
- ✅ Authentication Failure
- ✅ Invalid Intent
- ✅ Unsupported Queries
- ✅ Intent Modification

---

## 📸 Sample Conversation

```
User:
Hello

Assistant:
Please provide your User ID and PIN.

User:
User ID 5673 PIN 1234

Assistant:
Hi Devin, how can I help you today?

User:
Convert USD to INR for yesterday
and tell me the date of coming Sunday.

Assistant:
Detected:

1. Currency Conversion
2. Date Query

Shall I proceed?
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/Multi-Intent-AI-Assistant.git
```

### Install

- Docker Desktop
- Ollama
- n8n

### Pull Model

```bash
ollama pull llama3.1
```

### Start Ollama

```bash
ollama serve
```

### Start n8n

```bash
docker run -it --rm \
-p 5678:5678 \
-v n8n_data:/home/node/.n8n \
n8nio/n8n
```

Open

```
http://localhost:5678
```

Import the workflow and run it.

---

## 📖 Documentation

A complete project report is included in this repository.

The report contains:

- 📌 Project Overview
- 🏗️ Architecture Design
- 🔄 Complete Workflow Explanation
- 🧩 Every n8n Node Explained
- 🛠️ Step-by-Step Implementation Guide
- ⚙️ Engineering Decisions
- 📊 Evaluation Results
- 🚧 Limitations
- 🎯 Conclusion

If you want to understand **how this project was built from scratch**, refer to the project report included in this repository.

---

## 🎯 Future Improvements

- More Intent Types
- Voice Interface
- Real Database Authentication
- Email Support
- Calendar Integration
- Weather API
- Reminder Scheduling
- Better Local LLM Support

---

## 👨‍💻 Author

**Aditya Patil**

B.E. Computer Engineering

St. Francis Institute of Technology

Mumbai, India

---

## ⭐ If you like this project

Give it a ⭐ on GitHub if you found it useful!
