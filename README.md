# 🧾 n8n Telegram Dialogs Extractor

This powerful automation workflow for [n8n.io](https://n8n.io) allows you to **extract full text conversations from exported Telegram chats** (HTML + audio `.ogg` files) and convert them into clean, readable, and chronologically sorted JSON format. Ideal for journalists, researchers, or archiving your own history.

---

## 🚀 Features

- 🔄 Processes `messages.html` from Telegram export
- 🧠 Extracts sender name, message text, and timestamp
- 🗣️ Supports `.ogg` voice message transcription using **Groq + Whisper-v3**
- 🧹 Cleans, formats, and sorts dialogs
- 📁 Generates downloadable `dialog_YYYY-MM-DD_HH-MM-SS.json` with all extracted content

---

## 🛠 Technologies Used

- `n8n` visual automation builder
- `Python` Code Nodes for parsing and formatting
- `BeautifulSoup` for HTML parsing
- `Groq Whisper` AI for speech-to-text
- Multipart file handling & custom webhooks

---

## 💡 How It Works

1. Upload your exported Telegram ZIP archive via webhook
2. Workflow unpacks and filters `messages.html` and `.ogg` files
3. Extracts messages and metadata from HTML
4. Sends `.ogg` voice messages to Whisper model for transcription
5. Merges results, sorts by date/time, and exports structured `.json`

---

## 📦 Input Example

Telegram export ZIP containing:

```
messages.html
voice1.ogg
voice2.ogg
```

---

## 🧾 Output Example

```json
{
  "dialog": [
    {
      "author": "John Doe",
      "datetime": "12.04.2024 15:32:10",
      "text": "Hello, how are you?"
    },
    {
      "author": "Jane",
      "datetime": "12.04.2024 15:32:45",
      "text": "🎤 Voice: I'm good, thanks!"
    }
  ]
}
```

---

## 🔗 Profile & Services

💼 Created by [Serhii Litus (n8n Developer & AI Automator)](https://www.upwork.com/freelancers/~016b54c2291f96bd7d)

---

## 📥 How to Use

- Clone or import this workflow into your n8n instance
- Set up webhook trigger
- Export a Telegram chat from desktop client
- Upload the `.zip` via the webhook URL
- Download your structured `.json` chat data

---

## 📌 Use Cases

- 💬 Conversation Analysis
- 🧑‍⚖️ Legal or HR Documentation
- 📚 Personal Archiving
- 🎓 Research in Social Behavior

---

## 📧 Contact & Customization

Need help or want to build your own AI-enhanced data extraction workflow?

Created by [Serhii Litus](https://www.upwork.com/freelancers/~016b54c2291f96bd7d)  
Let's build smart automations that work while you sleep ☕ 
