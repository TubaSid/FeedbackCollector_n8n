# The Feedback Collector That Thinks - AI + n8n + Gemini
An AI-powered feedback automation workflow built using **n8n**, **Tally.so**, **Google Gemini (free API)**, **Slack**, **Gmail** and **Google Sheets**.

It automatically receives feedback submissions, classifies them using Gemini, filters gibberish or irrelevant text, sends formatted **Slack** alerts, replies to users via **Gmail** and logs everything neatly in **Google Sheets**, all in one compact workflow.

---

## What It Does

| Step | Action |
|------|---------|
| 1 | User submits a Tally form |
| 2 | n8n Webhook catches the data |
| 3 | Gemini classifies feedback type (Complaint, Compliment, Feature Request, Other) |
| 4 | Code node checks for gibberish or spam |
| 5 | Slack sends internal notification |
| 6 | Gmail sends an auto-reply to the user |
| 7 | Google Sheets logs structured data |
| 8 | Webhook responds to Tally |

---

## Read the Full Story

For a complete breakdown of how this workflow was built, from learning webhooks to designing the logic, read the full Medium article:  
[Read on Medium](https://tubasid.medium.com/from-confusion-to-automation-how-i-built-an-ai-powered-feedback-collector-in-n8n-with-gemini-74e2ea72d56f)

---

## How to Use the `.json` File

1. **Download** the exported workflow file (`Feedback Collector.json`).
2. Open **n8n** (Cloud or self-hosted).
3. Go to **Workflows → Import from File**.
4. Upload the `.json` file.
5. Update the following credentials:
   - **Gemini API key** → get from [Google AI Studio](https://aistudio.google.com/api-keys)
   - **Slack**, **Gmail** and **Google Sheets** credentials.
6. Use the **Production Webhook URL** inside your **Tally Form → Integrations → Webhooks**.
7. Click **Activate Workflow**.

Now every new Tally submission is automatically:
- Classified by Gemini  
- Filtered for gibberish or spam  
- Sent to the correct Slack channel  
- Responded to via Gmail  
- Logged into Google Sheets  

---

## Tech Stack

- **n8n** – Workflow automation  
- **Tally.so** – Front-end feedback form  
- **Google Gemini 2.0 Flash** – AI classification (Free)  
- **Slack** – Team notifications  
- **Gmail** – Auto-responses  
- **Google Sheets** – Feedback database  

---

Import, run, explore and learn how a simple feedback form can think for itself.
