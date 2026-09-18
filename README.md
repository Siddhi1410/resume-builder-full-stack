# 📄 AI Resume Builder

A full-stack AI-powered resume builder that lets users create, edit, and share professional resumes with multiple templates, AI-enhanced content, and real-time preview.

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-Express_5-339933?logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)
![Gemini AI](https://img.shields.io/badge/Gemini_AI-Powered-4285F4?logo=google&logoColor=white)

## ✨ Features

### 🤖 AI-Powered
- **AI Professional Summary** — Auto-generate compelling, ATS-friendly professional summaries
- **AI Job Description Enhancer** — Improve work experience descriptions with action verbs and quantifiable results
- **Resume Upload & Parse** — Upload existing PDF resumes and extract structured data using AI

### 📝 Resume Builder
- **Drag & Drop Sections** — Personal Info, Experience, Education, Projects, Skills
- **4 Professional Templates** — Classic, Modern, Minimal, and Minimal Image
- **Custom Accent Colors** — Personalize resume with a color picker
- **Profile Photo Upload** — Upload photos with optional AI background removal
- **Real-time Preview** — See changes instantly as you type

### 🔗 Share & Export
- **Public Resume Links** — Share resumes via public URLs
- **Print / Download PDF** — Export resumes as PDF using browser print

### 🔐 Authentication
- **JWT-based Auth** — Secure user registration and login
- **Protected Dashboard** — Manage all your resumes in one place

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React 19 | UI Library |
| Redux Toolkit | State Management |
| React Router v7 | Client-side Routing |
| Tailwind CSS 4 | Styling |
| Vite 7 | Build Tool |
| Axios | API Calls |
| Lucide React | Icons |
| React Hot Toast | Notifications |

### Backend
| Technology | Purpose |
|---|---|
| Node.js + Express 5 | REST API Server |
| MongoDB + Mongoose | Database |
| JWT | Authentication |
| ImageKit | Image Upload & Processing |
| Gemini AI (via OpenAI SDK) | AI Features |
| Multer | File Upload Handling |
| bcrypt | Password Hashing |

## 📁 Project Structure

```
resume-builder/
├── client/                    # React Frontend
│   ├── src/
│   │   ├── app/               # Redux store & slices
│   │   ├── components/
│   │   │   ├── home/          # Landing page components
│   │   │   ├── templates/     # Resume templates (4 templates)
│   │   │   ├── *Form.jsx      # Resume section forms
│   │   │   └── ...
│   │   ├── configs/           # API configuration
│   │   ├── pages/             # Route pages
│   │   └── assets/            # Static assets
│   └── ...
├── server/                    # Express Backend
│   ├── configs/               # DB, AI, ImageKit configs
│   ├── controllers/           # Route handlers
│   ├── middlewares/           # Auth middleware
│   ├── models/                # Mongoose schemas
│   ├── routes/                # API routes
│   └── server.js              # Entry point
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- MongoDB Atlas account
- ImageKit account
- Google AI (Gemini) API key

### 1. Clone the repository
```bash
git clone https://github.com/Siddhi1410/resume-builder-full-stack.git
cd resume-builder-full-stack
```

### 2. Setup Backend
```bash
cd server
npm install
```

Create a `.env` file in the `server/` directory (refer to `.env.example`):
```env
JWT_SECRET = "your_jwt_secret"
MONGODB_URI = "your_mongodb_connection_string"
IMAGEKIT_PRIVATE_KEY = "your_imagekit_private_key"
OPENAI_API_KEY = "your_gemini_api_key"
OPENAI_BASE_URL = "https://generativelanguage.googleapis.com/v1beta/openai/"
OPENAI_MODEL = "gemini-2.5-flash"
```

Start the server:
```bash
npm start
```

### 3. Setup Frontend
```bash
cd client
npm install
```

Create a `.env` file in the `client/` directory:
```env
VITE_BASE_URL = "http://localhost:3000"
```

Start the development server:
```bash
npm run dev
```

## 🌐 Deployment

- **Frontend**: Deployed on [Vercel](https://vercel.com)
- **Backend**: Deploy on [Render](https://render.com) / [Railway](https://railway.app)

## 📜 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/users/register` | Register a new user |
| POST | `/api/users/login` | Login user |
| GET | `/api/users/data` | Get user data |
| POST | `/api/resumes/create` | Create a new resume |
| GET | `/api/resumes/:resumeId` | Get resume by ID |
| PUT | `/api/resumes/update` | Update resume |
| DELETE | `/api/resumes/:resumeId` | Delete resume |
| GET | `/api/resumes/public/:resumeId` | Get public resume |
| POST | `/api/ai/enhance-pro-sum` | AI enhance professional summary |
| POST | `/api/ai/enhance-job-desc` | AI enhance job description |
| POST | `/api/ai/upload-resume` | Upload & parse resume with AI |

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
