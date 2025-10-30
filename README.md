# Smart-Lead-Capture-System
Public HTML form → Salesforce Lead record → automatic Thank-You email.

This project implements a **public Lead capture system** using **Salesforce Experience Cloud + Web-to-Lead**, allowing users to submit a form that directly creates a **Lead** record in Salesforce and triggers an automatic **Thank-You email**.  

This solution replicates a real-world marketing landing page and CRM integration pipeline.

---

## 🚀 Features

- ✅ Custom Lead form hosted on **Experience Cloud**
- ✅ **Web-to-Lead** Salesforce integration
- ✅ Leads automatically recorded in Salesforce CRM
- ✅ **Thank-You email** automation (Auto-Response Rule / Flow)
- ✅ **Success confirmation banner** (no extra page needed)
- ✅ Clean, responsive HTML/CSS form UI
- ✅ Debug mode for troubleshooting
- ✅ Self-redirect using `retURL` to show success status
- ✅ Follows Salesforce security best practices

**Flow:**  
`Experience Cloud Page → Web-to-Lead Form → Salesforce Leads → Auto-Email`

---

## 🛠️ Tech Stack

| Component | Technology |
|----------|-----------|
| CRM | Salesforce Sales Cloud |
| Portal | Salesforce **Experience Cloud** |
| Lead Capture | Web-to-Lead |
| Email | Auto-Response Rules / Flow |
| Frontend | HTML, CSS, JS |
| Hosting | Salesforce Experience Cloud |
| Optional | Python local server for testing |

---

## 📋 Prerequisites

Before setup:

- Salesforce Developer Org / Trailhead Playground
- **Experience Cloud enabled**
- **Web-to-Lead enabled**
- **Deliverability = All Email**
  - Setup → *Deliverability* → Access Level = **All Email**
- Org-Wide Email Address (optional)

---

## 🧩 Project Setup Steps

### ✅ 1. Enable Web-to-Lead  
**Setup → Web-to-Lead → Enable**

### ✅ 2. Enable Experience Cloud  
**Setup → Digital Experiences → Enable**

Create a new site & open Experience Builder.

### ✅ 3. Create Web-to-Lead Form  
**Setup → Web-to-Lead → Create Web-to-Lead Form**

Select fields like:  
- First Name  
- Last Name *(required by Salesforce)*  
- Company *(required)*  
- Email  
- City  
- Country  

Salesforce generates basic HTML.

### ✅ 4. Replace with modern UI form (this repo’s `leadform.html`)  

- Update `oid` with your Org ID
- Update `retURL` to your Experience Site page

### ✅ 5. Host Form in Experience Cloud  

In Experience Builder:  
**Drag “HTML” component → paste `leadform.html` code**

Publish site ✅

---

## 📧 Configure Auto-Response Email

### Option 1: **Auto-Response Rule** ✅ *(recommended)*

> Setup → Auto-Response Rules → Lead

Rule criteria:  
`Lead Source = Web`

Template example: 
<img width="571" height="269" alt="Screenshot 2025-10-30 at 6 57 54 PM" src="https://github.com/user-attachments/assets/a40aab41-503b-47e5-a949-b46bc1b98881" />


