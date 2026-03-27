# 🤖 SmartDesk AI

An AI-powered ticket management system that intelligently **categorizes, prioritizes, and assigns support tickets** to the most suitable moderators.

Built as part of the ChaiCode YouTube series, this project demonstrates how to integrate AI into real-world support workflows.

---

## 🚀 Overview

SmartDesk AI automates the entire ticket lifecycle using AI and event-driven architecture. It reduces manual effort, improves response time, and ensures tickets reach the right person faster.

---

## ✨ Key Features

### 🧠 AI-Powered Ticket Processing
- Automatic ticket categorization  
- Smart priority assignment  
- Skill extraction from ticket content  
- AI-generated notes for moderators  

### 👨‍💻 Intelligent Assignment
- Skill-based moderator matching  
- Regex-powered routing system  
- Fallback to admin if no match found  

### 👥 User Management
- Role-based access control (User / Moderator / Admin)  
- Moderator skill management  
- Secure JWT authentication  

### ⚙️ Background Processing
- Event-driven workflows using Inngest  
- Asynchronous ticket processing  
- Automated email notifications  

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express  
- **Database**: MongoDB  
- **Authentication**: JWT  
- **AI Integration**: Google Gemini API  
- **Background Jobs**: Inngest  
- **Email**: Nodemailer (Mailtrap)  
- **Dev Tools**: Nodemon  

---

## 📦 Prerequisites

- Node.js (v14 or higher)  
- MongoDB  
- Google Gemini API key  
- Mailtrap account  

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/smartdesk-ai.git
cd smartdesk-ai

2. Install dependencies
npm install

3. Environment Setup

Create a .env file:

MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
MAILTRAP_SMTP_HOST=your_host
MAILTRAP_SMTP_PORT=your_port
MAILTRAP_SMTP_USER=your_user
MAILTRAP_SMTP_PASS=your_password
GEMINI_API_KEY=your_api_key
APP_URL=http://localhost:3000

▶️ Running the Application
Start backend server
npm run dev
Start Inngest dev server
npm run inngest-dev

Inngest runs at: http://localhost:8288

📡 API Endpoints

Authentication
POST /api/auth/signup → Register user
POST /api/auth/login → Login & get JWT

Tickets
POST /api/tickets → Create ticket
GET /api/tickets → Get user tickets
GET /api/tickets/:id → Get ticket details

Admin
GET /api/auth/users → Get all users
POST /api/auth/update-user → Update roles & skills

🔄 Ticket Workflow
User submits a ticket
AI processes the ticket (skills, priority, notes)
System assigns moderator
Email notification is sent

📚 Dependencies
express
mongoose
jsonwebtoken
bcrypt
dotenv
cors
inngest
nodemailer
