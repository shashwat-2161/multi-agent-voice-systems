# 📞 Automated Outbound Call System with Airtable & Twilio

This project automates outbound calls to leads stored in Airtable using Twilio and updates lead statuses based on the outcome of those calls. It also records each call’s details in a separate "Call Records" table for tracking and analysis.

---

## 🔧 Features

- ✅ Fetches leads from Airtable with status **TBC**
- 🔄 Updates status to **In-Progress** before initiating call
- ☎️ Uses Twilio to trigger outbound calls with a voice agent
- 🧠 Receives call status updates (via webhook)
- 🗂 Updates lead status (e.g., Called, Failed) in Airtable
- 📝 Logs call metadata and transcript in the **Call Records** table

---

📋 Airtable Schema Expectations
🔹 Leads Table (Leads)
Field Name        -        Type        -        Description
Mobile                Phone	Customer's        phone number
Status	              Single select	          "TBC", "In-Progress", "Called", "Failed"
Attempt               	Number	              Times the lead has been contacted
🔹 Call Records Table (Call Records)
Field Name        -        Type        -        Description
callproviderID	           Text	               Call SID from Twilio
customernumber	          Phone	               Customer’s phone number
type	                    Text	                   "Outbound"
started	                 DateTime	                Call start time
ended	                   DateTime	                Call end time
endedreason	              Text	               Call outcome from Twilio
transcript            	Long Text	              Transcription of call
Duration	                Number	            Length of the call in seconds

---

Vapi Setup
1. Model
![Screenshot 2025-04-09 212836](https://github.com/user-attachments/assets/0a2a3eee-13a5-4105-8844-4cc7ec24ffe9)
2. Transcriber
![image](https://github.com/user-attachments/assets/0e495eee-f43d-4df3-9845-5e65c1311e9b)
3. Voice
![image](https://github.com/user-attachments/assets/ef69aa43-25f3-4e96-8de6-8de11e29a476)
4. Messaging
![image](https://github.com/user-attachments/assets/0b8873ed-b7d7-4ef4-93d9-54bcf8aa705d)
![image](https://github.com/user-attachments/assets/79d4c010-4a6d-485e-8d2f-271c42b71cd6)

---

n8n Workflow
1. Workflow 1
![image](https://github.com/user-attachments/assets/38b3eda3-8e9c-454b-9fe9-691c81527e75)

2. Workflow 2
![image](https://github.com/user-attachments/assets/ce555dec-d0ce-43ca-bd59-7a67dfbb2e8a)


---

Video explanation link 

---


