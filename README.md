# 🤖 AI Resume Analyzer

> AI-powered resume analyzer that scores your resume 
> against any job description using Claude Sonnet 4.



---

## 🚀 What It Does

Upload your resume as a PDF and paste a job description.
The app converts your resume to an image, sends it to 
Claude Sonnet 4 AI, and gets back:

- ✅ ATS compatibility score
- ✅ Keyword match analysis  
- ✅ Role-specific improvement suggestions
- ✅ Detailed feedback on what to fix

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | React Router v7 (Full-Stack SSR) |
| Language | TypeScript |
| Frontend | React 19, Tailwind CSS v4 |
| AI | Claude Sonnet 4 via Puter.js |
| PDF Processing | pdfjs-dist (PDF → Image conversion) |
| State Management | Zustand |
| File Upload | react-dropzone |
| Auth & Storage | Puter.js (Auth + Cloud Filesystem + KV Store) |
| Build Tool | Vite |
| Deployment | Docker + Vercel |

---

## ✨ Key Features

- **PDF to Image Conversion** — Uses pdfjs-dist to render 
  resume pages as images directly in the browser
- **Claude Sonnet 4 Analysis** — Sends resume image + job 
  description to Claude for intelligent ATS scoring
- **Analysis History** — Saves results using Puter.js KV 
  store so users can access previous analyses
- **User Authentication** — Built-in auth via Puter.js
- **Docker Ready** — Containerized for any cloud deployment

---

## 🏗️ Architecture
User uploads PDF
↓
pdfjs-dist converts PDF → Image (browser)
↓
Image + Job Description sent to Puter.js AI
↓
Claude Sonnet 4 analyzes resume vs job description
↓
ATS Score + Feedback returned to user
↓
Results saved to Puter.js KV Store

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repo
git clone https://github.com/rudra-webdev/ai-resume-analyzer

# Install dependencies
cd ai-resume-analyzer
npm install

# Start development server
npm run dev
```

App runs at `http://localhost:5173`

### Docker Deployment

```bash
# Build image
docker build -t ai-resume-analyzer .

# Run container
docker run -p 3000:3000 ai-resume-analyzer
```

---

## 📁 Project Structure
ai-resume-analyzer/
├── app/
│   ├── routes/          # Page components
│   ├── lib/             # Core utilities
│   │   ├── puter.ts     # Puter.js AI integration
│   │   └── pdf2img.ts   # PDF to image conversion
│   └── components/      # Reusable UI components
├── types/               # TypeScript definitions
├── public/              # Static assets
├── Dockerfile           # Docker configuration
└── vite.config.ts       # Build configuration

## 🎯 What I Learned

- Full-stack development with React Router v7 SSR
- PDF processing in the browser using pdfjs-dist
- Integrating Claude Sonnet 4 for document analysis
- TypeScript for type-safe React development
- Docker containerization and deployment
- State management with Zustand
