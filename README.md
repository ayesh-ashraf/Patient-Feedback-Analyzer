# Patient-Feedback-Analyzer
An n8n workflow that analyzes the  patient feedback using AI and automates email notifications
# FB Analyzer – Automated Patient Feedback Sentiment System (n8n)
This project uses **n8n** to automatically analyze patient feedback and send categorized email notifications based on sentiment (positive, neutral, or negative).
**Features**
- Automatically captures feedback from a Webhook (e.g., Google Forms, Sheets, etc.)
- Performs **Sentiment Analysis** using OpenAI
- Sends categorized feedback reports via **Gmail**
- Structured, modular, and ready for automation testing

## Workflow Overview
### Components:
1. **Webhook** – Receives patient feedback data.
2. **Edit Fields** – Formats the incoming data.
3. **Sentiment Analysis** – Uses OpenAI Chat Model to determine if feedback is positive, negative, or neutral.
4. **Edit Fields + Message Models** – Prepares personalized messages for each sentiment type.
5. **Merge + Gmail Nodes** – Combines processed data and sends automatic notification emails.

## Setup Instructions

### Requirements
- n8n (self-hosted or cloud)
- OpenAI API key
- Gmail credentials (OAuth or App Password)
- Ngrok (optional for public webhook testing)

### Steps
1. Clone this repository  
2. Import workflow.json into your n8n instance:
Click “Import from file” in n8n
Select the workflow.json file
3. Configure your API keys and email credentials inside n8n nodes.
4.Execute the workflow to test.
### ** Example Input **
{
  "timestamp": "2025-10-21T15:30:00Z",
  "patient_id": "12345",
  "source": "Google Form",
  "text": "The doctor was very kind and professional!"
}

   

