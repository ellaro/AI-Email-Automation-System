from pathlib import Path

readme_content = """# 📩 AI Email Automation System (Power Automate)

An intelligent email automation workflow built using Microsoft Power Automate that processes incoming emails, applies conditional logic, and integrates with external APIs.

---

## 🚀 Overview

This project demonstrates how to build an end-to-end automation flow triggered by incoming Outlook emails.  
The system filters relevant emails (e.g., support requests), sends structured data to an external API, and simulates backend processing using webhook endpoints.

---

## 🧠 Key Features

- 📥 Triggered automatically when a new email arrives (Outlook)
- 🔍 Conditional logic to filter relevant emails (e.g., "Support", "Request")
- 🌐 Integration with external APIs using HTTP POST requests
- 📡 Real-time data transmission using JSON payloads
- 🧪 Webhook simulation for backend processing (via webhook.site)
- ⚙️ End-to-end automation workflow design

---

## 🏗️ Architecture

Outlook Email Trigger → HTTP Request → Condition → HTTP (POST) → Compose

---

## 🛠️ Technologies Used

- Microsoft Power Automate
- Outlook (Microsoft 365)
- HTTP / REST APIs
- JSON
- Webhook.site (for testing API calls)

---

## ⚙️ How It Works

1. A new email is received in Outlook  
2. The system checks if the subject contains keywords like:
   - Support
   - Request
3. If TRUE:
   - Sends a POST request to an external API (webhook)
   - Includes structured JSON data:
     {
       "from": "email sender",
       "subject": "email subject",
       "body": "email content"
     }
   - Processes the response using Compose
4. If FALSE:
   - The email is ignored

---

## 📸 Screenshots

(Add screenshots of your flow here)

---

## 🧪 How to Run

1. Create a Power Automate account  
2. Create a new Automated Cloud Flow  
3. Add trigger: When a new email arrives (Outlook)  
4. Add condition: Subject contains "Support" or "Request"  
5. Add HTTP action (POST) to webhook.site  
6. Test by sending an email  

---

## 💡 What This Project Demonstrates

- Automation design using event-driven architecture  
- API integration using HTTP requests  
- Working with structured data (JSON)  
- Building real-world workflows using Microsoft ecosystem tools  

---

## 👩‍💻 Author

Ella Rosenberg  
GitHub: https://github.com/ellaro  
LinkedIn: https://www.linkedin.com/in/ella-rosenberg-developer  

---

## 🚀 Future Improvements

- Integrate with real backend (Flask / Azure Functions)  
- Add AI processing (text classification / summarization)  
- Store results in a database  

---

⭐ If you found this project useful — feel free to star it!
"""

file_path = Path('/mnt/data/README_AI_Email_Automation.md')
file_path.write_text(readme_content)

file_path
