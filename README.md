***
# CodeGenie - AI-Powered Code Explanation & Generation Platform

CodeGenie is an AI-driven platform designed to help students, developers, educators, and teams work smarter and faster. It offers a seamless and secure environment for understanding, generating, and analyzing code across multiple programming languages, combining strong authentication, AI models, user tracking, feedback systems, and admin management in a single cohesive application.

## Why CodeGenie?

Modern developers read and write more code than ever before. CodeGenie simplifies this by providing:

- Clear, human-readable explanations of code snippets in English
- High-quality AI-generated code from natural language prompts
- A full history of user activity and generated content
- A powerful admin dashboard with detailed analytics and control
- Secure, role-based authentication and recovery tools

It is the perfect environment for both learning and professional coding.

## Features

### Authentication & Account Security
- Secure login/signup using JWT
- Email and password verification with password hashing
- Optional email verification and role-based permissions (Admin, User)
- Access and refresh token handling with auto-refresh
- OTP-based password recovery through Gmail SMTP
- Optional security questions for fallback recovery
<img width="2398" height="1058" alt="image" src="https://github.com/user-attachments/assets/678e4122-03fc-4c46-86f4-960673781c48" />


### User Dashboard
- **Code Explanation Engine:** Paste code (Python, JavaScript, SQL) and receive clear, structured explanations using AST and token parsing techniques
- **Code Generator:** Generate working code using AI models such as CodeLlama, StarCoder2, and DeepSeek-Coder based on your description
- **History:** Track all generated code, explanations, chats, and usage details with timestamps and model info
- **Profile Settings:** Manage user information, themes, and secure password changes with OTP and security questions
<img width="2531" height="1240" alt="image" src="https://github.com/user-attachments/assets/83990fb2-50a9-4c40-bf7b-9003109d434e" />
  
### Admin Dashboard
- Manage user roles and promote users to admin (max 2 admins for security)
- Reset user passwords and view a global activity log
- Monitor system health, usage patterns, and analytics on user growth and AI models
- Search across users, code histories, feedback, and generated snippets
- Analyze feedback sentiment and module usage metrics
<img width="2510" height="1184" alt="image" src="https://github.com/user-attachments/assets/7b413023-42b7-44f9-a5a7-535cb5742489" />

## Project Structure

```
CodeGenie/
│
├── app.py                       # Streamlit frontend UI and navigation
│
├── backend/
│   ├── auth.py                  # JWT authentication and security logic
│   ├── generator.py             # AI code generation engine
│   ├── explainer.py             # Code explanation engine
│   ├── models.py                # Database schema and helpers
│   ├── history.py               # User activity logging
│   ├── feedback.py              # Reviews and sentiment analysis
│   └── admin.py                 # Admin controls and analytics
│
├── requirements.txt             # Python dependencies
├── .env.example                 # Environment variable template
└── README.md
```

## How to Run

1. Clone the repository  
   `git clone https://github.com/yourusername/CodeGenie.git`  
   `cd CodeGenie`

2. Configure environment variables  
   Copy `.env.example` to `.env` and add your JWT secrets, Gmail SMTP credentials, admin email, database paths, etc.

3. Start the application  
   `streamlit run app.py`

## Security

CodeGenie prioritizes security with JWT access and refresh tokens, role-based access control, password hashing, OTP recovery, and a strict admin limit. All user actions are logged for auditability.

***
