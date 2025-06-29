# 📱 WhatsApp AI Agent

**WhatsApp AI Agent** is a custom-built solution that connects your WhatsApp account to powerful AI conversations using **n8n**, Docker, and OpenRouter AI.

---

## 🚀 What It Does

✅ Connects to WhatsApp to send and receive messages automatically  
✅ Handles:
- Text messages
- Voice notes (transcribed and answered)
- Images and PDF documents (analyzed and summarized)

✅ Uses **OpenRouter AI** for intelligent, context-aware replies  
✅ Remembers conversations for each user to maintain context  
✅ Allows you to build custom workflows for:
- Answering FAQs
- Qualifying leads
- Scheduling meetings
- Sending dynamic business info

---

## ⚙️ How It Works

1. WhatsApp messages are received in **n8n** via WhatsApp integration.
2. Messages are routed depending on type (text, audio, images, PDFs).
3. Content is sent to **OpenRouter AI** for smart replies.
4. Replies are sent back automatically to the user on WhatsApp.
5. All runs smoothly inside Docker containers for easy deployment.

---

## 💻 How to Get Started

```bash
git clone https://github.com/sammakwana/WhatsApp-AI-Agent.git
cd WhatsApp-AI-Agent

# Add your environment variables (.env file)

docker-compose up -d
```

- Open n8n in your browser.
- Scan the WhatsApp QR code.
- Start chatting and watch the AI respond!

---


## 🔗 Links

- **GitHub Repository:** [WhatsApp-AI-Agent](https://github.com/sammakwana/WhatsApp-AI-Agent)

---


# Build Your First AI Agent — Step-by-Step Guide

### 1️⃣ Install Docker

First, download and install **Docker** on your machine.

---

### 2️⃣ Run n8n Using Docker

Open your terminal and run the following commands:

```bash

docker pull n8nio/n8n

```

```bash
docker run -it --rm \
-p 5678:5678 \
-v ~/.n8n:/home/node/.n8n \
n8nio/n8n

```

You can also manage n8n using:

```bash
docker start n8n
docker stop n8n

```

Once running, access n8n in your browser at:

👉 [http://localhost:5678](http://localhost:5678/)

---

### 3️⃣ Set Up Your n8n Account

Follow the on-screen instructions to set up your n8n account.

---

### 4️⃣ Install VS Code

Download and install **Visual Studio Code** for writing and editing your code.

---

### 5️⃣ Install Required Packages

1. Install **Node.js** — this will also install **npm**.
2. Open your terminal and install the necessary packages:

```bash
npm install express venom-bot axios

```

---

### 6️⃣ Import Your Code

Copy your bot code into your VS Code project.

---

### 7️⃣ Import Your Agent Workflow into n8n

Upload the provided `.json` file to n8n to load your AI agent workflow.

---

### 8️⃣ Create a Test Function

Set up a test function to simulate interactions with your agent.

---

---

### 9️⃣ Setup Openrouter account

Set up your api key. And add your api key into your n8n credentials.

---

### 🔟 Test Your Workflow

1. **Enable workflow testing** in n8n.
2. Run your bot with:

```bash
node bot.js

```

1. Trigger the test using `curl`:

```bash
curl -X POST http://localhost:3000/simulate-self \
-H "Content-Type: application/json" \
-d '{"body": "Hi", "from": "your-phone-number@c.us"}'

```

---

✅ Done! Your AI agent is now ready for action.

**Created with ❤️ by Samir Makwana**
