# 🛡️ WISP – Women’s Intelligent Safety Partner

WISP is an AI-powered chatbot designed to support women facing safety concerns in the workplace, during travel, online, or in public spaces. Powered by Rasa and enhanced with voice capabilities, WISP aims to be an accessible, intelligent safety assistant for every woman.

---

## ✨ Features

- 💼 **Women at the Workplace**  
  Provides guidance and support for professional safety issues.

- 🕵️ **Cybercrime**  
  Helps report and respond to online harassment and abuse.

- 👀 **Eve Teasing**  
  Offers assistance for harassment in public spaces.

- 🚗 **Safe Travel**  
  Enables location tracking and real-time emergency alerts during travel.

---

## 🛠 Technologies Used

- **Python** – Core programming language  
- **Rasa** – For NLP, intent recognition, and dialogue flow  
- **Flask** – Serves the web interface  
- **pyttsx3** – Text-to-speech for audio responses  
- **SpeechRecognition** – Enables voice input  
- **gTTS** – Google Text-to-Speech support  
- **spaCy** – (Optional) Enhances natural language understanding  

---

## 🚀 Installation Guide

### 1. Prerequisites

Ensure the following are installed:

- Python 3.6 – 3.8  
- pip (Python package installer)  
- Virtual environment tool (optional but recommended)  
- Rasa (v3.1.1 recommended)  
- Flask  
- pyttsx3  
- SpeechRecognition  
- gTTS  
- spaCy (and optionally, its English model)

### 2. Setup Steps

```bash
# Navigate to the project directory
cd projectname

# Create and activate a virtual environment
python3 -m venv env
# On Windows:
env\Scripts\activate
# On macOS/Linux:
source env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

---

## ▶️ Usage

### 1. Train the Rasa model

```bash
rasa train
```

### 2. Run the custom action server

```bash
rasa run actions
```

### 3. Start the Rasa chatbot server

```bash
rasa run -m models --enable-api --cors "*"
```

### 4. Launch the web application

```bash
python app.py
```

---

## 🌐 Web Deployment (Optional)

To make the chatbot accessible on the web:

- Use [ngrok](https://ngrok.com/) to expose your Rasa server:
  ```bash
  ngrok http 5005
  ```
- Update your web interface (`index.html`) to use the ngrok URL for `socketUrl`.

---
