# AI Chat Agent Workflow (n8n)

This repository contains an **n8n workflow** that demonstrates how to build an AI-powered chat agent using **LangChain**, **OpenAI**, and **Gmail integration**.

The workflow listens for chat messages, processes them using an AI agent with short-term memory, and can optionally send emails through Gmail when instructed.

---

## What this workflow does

* Receives a chat message via n8n Chat Trigger
* Uses an AI Agent powered by OpenAI (`gpt-4.1-mini`)
* Maintains short-term conversation memory (last 10 messages)
* Allows the AI Agent to send emails using Gmail as a tool
* Keeps the workflow inactive by default for safety

---

## Nodes used

* **Chat Trigger** – Starts the workflow when a chat message is received
* **AI Agent (LangChain)** – Controls reasoning and tool usage
* **OpenAI Chat Model** – Generates responses
* **Memory Buffer Window** – Stores recent conversation context
* **Gmail Tool** – Sends emails when explicitly triggered by the agent

---

## Credentials and security

* ❌ No API keys or OAuth tokens are included
* ❌ No live credentials are stored in this repository
* ✅ Credential placeholders are used (`REPLACE_ME`)
* ✅ Webhook IDs are intentionally removed

You must configure your own credentials inside n8n before running the workflow.

---

## How to use this workflow

1. Clone or download this repository
2. Open your **n8n dashboard**
3. Go to **Workflows → Import from file**
4. Import the provided JSON workflow
5. Add your own:

   * OpenAI API credentials
   * Gmail OAuth credentials
6. Activate the workflow

---

## Recommended agent behavior

For safety and control, it is recommended to configure the AI Agent with rules such as:

* Only send emails when the user explicitly asks
* Ask for confirmation before sending emails
* Do not send emails if recipient or subject is missing

---

## Use cases

* AI-powered email assistant
* Chat-to-email automation
* Learning project for n8n + LangChain
* Portfolio demonstration of AI automation skills

---

## Disclaimer

This workflow is provided for **learning and demonstration purposes**. Always review AI-generated actions carefully before using them in production.

---

## Author

Created as a learning and portfolio project using n8n and AI automation tools.
