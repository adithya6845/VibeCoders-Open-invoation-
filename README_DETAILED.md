# 🏥 MedHelp - Comprehensive Healthcare AI Platform

> **Advanced AI-powered medical diagnostic and analysis platform** featuring multiple specialized healthcare modules for brain MRI analysis, skin condition detection, and interactive medical diagnostics.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.11+-blue.svg)
![Node.js](https://img.shields.io/badge/node.js-16+-green.svg)
![TypeScript](https://img.shields.io/badge/typescript-5.0+-blue.svg)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Modules](#modules)
- [Installation & Setup](#installation--setup)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Development](#development)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

MedHelp is a comprehensive healthcare AI platform that integrates multiple specialized AI models for medical diagnosis and analysis. The platform combines:

- **Brain MRI Analysis** - AI-powered Alzheimer's risk detection
- **Interactive Medical Diagnostics** - Real-time symptom assessment with 3D medical visualization
- **Skin Analysis** - Advanced dermatological condition detection
- **Clinical Decision Support** - Evidence-based diagnostic recommendations

Built with modern web technologies (React, TypeScript, Three.js) and backend services (Flask, OpenAI/OpenRouter APIs), MedHelp demonstrates how AI can augment clinical decision-making while maintaining accuracy and usability.

---

## 📁 Project Structure

```
medhelp-platform/
│
├── 📂 backend/                    # Main API server (Flask)
│   ├── app.py                     # Flask application & MRI analysis API
│   ├── requirements.txt           # Python dependencies
│   ├── .env.example              # Environment template
│   └── test_openrouter.py        # Model testing utilities
│
├── 📂 frontend/                   # Legacy frontend
│   └── index.html                # Basic HTML interface
│
├── 📂 medhelp/                    # Primary TypeScript/React app
│   ├── src/
│   │   ├── main.ts               # Application entry point
│   │   ├── diagnostics.ts        # Medical diagnostic engine
│   │   ├── doctor-main.ts        # Doctor dashboard
│   │   ├── landing.ts            # Landing page logic
│   │   ├── title-reveal.ts       # UI animations
│   │   ├── style.css             # Global styles
│   │   │
│   │   ├── 📂 chatbot/           # Symptom assessment module
│   │   │   ├── chatbot-ui.ts     # Chat interface
│   │   │   ├── diagnostic-engine.ts  # Logic engine
│   │   │   └── symptom-data.ts   # Symptom database
│   │   │
│   │   ├── 📂 narrator/          # Medical narrator system
│   │   │   ├── narrator.ts       # Narration logic
│   │   │   └── narration-data.ts # Clinical descriptions
│   │   │
│   │   ├── 📂 viewer/            # 3D medical viewer
│   │   │   ├── scene.ts          # Three.js scene setup
│   │   │   ├── model.ts          # 3D model handling
│   │   │   └── animations.ts     # Visual effects
│   │   │
│   │   ├── 📂 assets/            # UI assets
│   │   │   ├── hero.png
│   │   │   ├── vite.svg
│   │   │   └── typescript.svg
│   │   │
│   │   └── 📂 chatbot/           # Advanced chat UI
│   │
│   ├── public/
│   │   ├── favicon.svg
│   │   ├── icons.svg
│   │   └── 📂 models/            # 3D medical models
│   │       └── *.fbx (3D files)
│   │
│   ├── package.json              # Node dependencies
│   ├── tsconfig.json             # TypeScript config
│   ├── vite.config.js            # Build configuration
│   └── index.html                # HTML entry point
│
├── 📂 Alzimer.ai/                # Specialized Alzheimer's module
│   ├── backend/
│   │   ├── app.py
│   │   ├── requirements.txt
│   │   └── test_openrouter.py
│   └── frontend/
│       └── index.html
│
├── 📂 Skin ai/                   # Dermatological analysis module
│   ├── backend/
│   │   ├── app.py
│   │   ├── requirements.txt
│   │   └── test_openrouter.py
│   └── frontend/
│       └── index.html
│
├── .env                          # Environment variables (create from .env.example)
├── .gitignore                    # Git ignore rules
├── README.md                     # Original readme
├── README_DETAILED.md            # This file
└── requirements.txt              # Root Python dependencies

```

---

## ✨ Features

### 🧠 Brain MRI Analysis Module
- **Advanced MRI Interpretation** - AI-powered analysis using vision models
- **Alzheimer's Risk Assessment** - Cognitive decline indicators
- **Clinical Biomarkers** - Detection of neuroimaging markers
- **Differential Diagnosis** - Multiple diagnostic possibilities
- **Structured Reports** - JSON-formatted clinical findings

### 🔍 Interactive Diagnostics (MedHelp)
- **Symptom Chatbot** - Multi-turn conversation for symptom assessment
- **Real-time Analysis** - Instant diagnostic suggestions
- **3D Medical Visualization** - Interactive human anatomy viewer
- **Clinical Database** - Comprehensive symptom-disease mapping
- **Evidence-based Recommendations** - Science-backed diagnostic paths

### 🏥 Skin Analysis Module
- **Dermatological Assessment** - Skin condition detection
- **Image Analysis** - Computer vision-based evaluation
- **Clinical Guidance** - Professional recommendations

### 🎨 User Experience
- Responsive design with Tailwind CSS
- Interactive 3D medical models (Three.js)
- Smooth animations (GSAP)
- Doctor dashboard & patient interface
- Real-time clinical narratives

---

## 🛠️ Technology Stack

### Backend
| Technology | Purpose | Version |
|-----------|---------|---------|
| Python | Server language | 3.11+ |
| Flask | Web framework | Latest |
| OpenRouter API | LLM access | - |
| OpenAI GPT-4o | Vision analysis | Latest |

### Frontend
| Technology | Purpose | Version |
|-----------|---------|---------|
| TypeScript | Language | 5.0+ |
| Vite | Build tool | 8.0+ |
| Three.js | 3D rendering | 0.183+ |
| Tailwind CSS | Styling | 4.2+ |
| GSAP | Animations | 3.14+ |

### Development & DevOps
| Tool | Purpose |
|------|---------|
| Node.js | Package management |
| npm | Dependency management |
| Git | Version control |

---

## 📦 Modules

### 1. **Core Platform (MedHelp)**
Interactive medical diagnostic system with real-time analysis.

**Features:**
- Symptom assessment chatbot
- Medical narrator system
- 3D anatomical visualization
- Interactive patient interface

**Entry Point:** `medhelp/index.html` or `npm run dev` in medhelp/

---

### 2. **Brain MRI Analysis (Alzimer.ai + Backend)**
Specialized module for Alzheimer's disease detection from brain MRI scans.

**Features:**
- Brain MRI image upload
- AI-powered structural analysis
- Cognitive risk assessment
- Clinical biomarker detection

**Entry Point:** `backend/app.py` → Flask server at `http://localhost:5000`

---

### 3. **Skin Analysis (Skin ai)**
Dermatological condition detection and assessment.

**Features:**
- Skin lesion analysis
- Condition classification
- Clinical recommendations

**Entry Point:** `Skin ai/backend/app.py`

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.11+
- Node.js 16+
- Git
- API Keys:
  - OpenRouter API Key (free tier available)
  - Optional: Anthropic Claude API Key

### Step 1: Clone or Download Repository
```bash
cd "medhelp new"
```

### Step 2: Backend Setup

#### Option A: Main Backend (Brain MRI Analysis)
```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
copy .env.example .env  # Windows
# or
cp .env.example .env    # macOS/Linux

# Add your API keys to .env
# OPENROUTER_API_KEY=your_key_here
# ANTHROPIC_API_KEY=your_key_here (optional)

# Run server
python app.py
```

#### Option B: Alzheimer's Specialized Module
```bash
cd Alzimer.ai/backend

python -m venv venv
venv\Scripts\activate  # or: source venv/bin/activate

pip install -r requirements.txt

# Configure .env
python app.py
```

#### Option C: Skin Analysis Module
```bash
cd Skin\ ai/backend

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
python app.py
```

### Step 3: Frontend Setup

#### For Main MedHelp Application
```bash
cd medhelp

# Install dependencies
npm install

# Development server (with hot reload)
npm run dev

# Production build
npm run build

# Preview production build
npm preview
```

#### For Legacy Frontend
```bash
# Simply open in browser
open frontend/index.html  # macOS
# or
start frontend/index.html # Windows
# or
xdg-open frontend/index.html # Linux
```

---

## ⚙️ Configuration

### Environment Variables (.env)

Create a `.env` file in the root and each backend folder:

```env
# API Keys
OPENROUTER_API_KEY=your_openrouter_api_key_here
ANTHROPIC_API_KEY=your_anthropic_key_here

# Server Configuration
FLASK_ENV=development
FLASK_DEBUG=True
PORT=5000

# API Configuration
API_MODEL=openai/gpt-4o-mini
MAX_TOKENS=1500
TEMPERATURE=0.7

# Frontend
VITE_API_URL=http://localhost:5000
```

### Getting API Keys

#### OpenRouter (Recommended - Free Tier Available)
1. Visit https://openrouter.ai
2. Sign up / Log in
3. Navigate to **API Keys**
4. Create new key
5. Copy and add to `.env`

**Benefits:**
- Free tier available
- Multiple model access
- No credit card required initially
- Flexible pricing

#### Anthropic Claude (Alternative)
1. Visit https://console.anthropic.com
2. Sign up / Log in
3. Go to **API Keys** → **Create Key**
4. Copy key (starts with `sk-ant-...`)
5. Add to `.env`

---

## 📖 Usage

### Brain MRI Analysis API

#### Upload and Analyze MRI
```bash
# Request
curl -X POST http://localhost:5000/api/analyze \
  -H "Content-Type: application/json" \
  -d '{
    "image": "base64_encoded_image_data",
    "media_type": "image/jpeg",
    "patient": {
      "age": 72,
      "sex": "Male",
      "mmse": 24,
      "family_history": "Yes",
      "symptoms": "Memory loss, confusion",
      "duration": "6 months"
    }
  }'
```

#### Response (JSON)
```json
{
  "success": true,
  "report": {
    "risk_level": "Moderate",
    "confidence": "High",
    "imaging_findings": "Mild hippocampal atrophy...",
    "biomarkers": ["Hippocampal atrophy", "Amyloid markers", "Tau pathology"],
    "cognitive_assessment": "Cognitive decline consistent with early stages...",
    "differential_diagnosis": ["Mild cognitive impairment", "Early Alzheimer's disease", "Vascular dementia"],
    "next_steps": ["Neuropsychological testing", "Biomarker testing", "Follow-up MRI in 12 months", "Cognitive training program"],
    "summary": "MRI shows mild structural changes consistent with early cognitive decline. Recommend biomarker testing and neuropsychological evaluation."
  }
}
```

### Interactive Diagnostics (MedHelp)

1. Open `medhelp/index.html` in browser or run `npm run dev`
2. Select symptoms from the chatbot
3. View AI diagnostic recommendations
4. Explore 3D anatomical visualizations
5. Access clinical narratives

### Health Check
```bash
curl http://localhost:5000/api/health
# Response: {"status": "ok", "model": "Alzmind v1.0 (OpenRouter)"}
```

---

## 📡 API Documentation

### Endpoints

#### POST `/api/analyze`
Analyzes brain MRI images with patient context.

**Parameters:**
- `image` (string, base64) - Base64-encoded image data
- `media_type` (string) - MIME type (default: "image/jpeg")
- `patient` (object) - Patient information:
  - `age` (number)
  - `sex` (string)
  - `mmse` (number) - Mini-Mental State Exam score
  - `family_history` (string)
  - `symptoms` (string)
  - `duration` (string)

**Returns:**
- Clinical analysis report with risk assessment and recommendations

---

#### GET `/api/health`
Health check endpoint.

**Returns:**
```json
{
  "status": "ok",
  "model": "Alzmind v1.0 (OpenRouter)"
}
```

---

## 🔧 Development

### Project Scripts

#### Backend
```bash
# Run analysis tests
python backend/test_openrouter.py

# Check model availability
python backend/check_models.py

# Validate API key
python backend/check_key.py
```

#### Frontend
```bash
# Development server with hot reload
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

### Code Structure

#### Diagnostic Engine (`medhelp/src/chatbot/diagnostic-engine.ts`)
- Symptom-disease mapping logic
- Risk calculation algorithms
- Evidence-based recommendations

#### 3D Viewer (`medhelp/src/viewer/`)
- Three.js scene initialization
- Model loading and animation
- Interactive controls

#### Narrator System (`medhelp/src/narrator/`)
- Clinical text generation
- Evidence-based descriptions
- Multi-language support (extensible)

---

## 🧪 Testing

### Test Image Upload
```python
# backend/test_openrouter.py
python test_openrouter.py
```

### Test API Endpoints
```bash
# Health check
curl http://localhost:5000/api/health

# Analyze sample image (requires base64 encoding)
python -c "
import requests
import base64

with open('sample_mri.jpg', 'rb') as f:
    image_b64 = base64.b64encode(f.read()).decode()

response = requests.post(
    'http://localhost:5000/api/analyze',
    json={
        'image': image_b64,
        'media_type': 'image/jpeg',
        'patient': {'age': 72, 'sex': 'Male'}
    }
)
print(response.json())
"
```

---

## 🌐 Deployment

### Backend (Flask API)

#### Using Gunicorn (Production)
```bash
# Install Gunicorn
pip install gunicorn

# Run with Gunicorn
gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

#### Docker (Optional)
```dockerfile
FROM python:3.11-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5000", "app:app"]
```

### Frontend (MedHelp)

#### Static Hosting
```bash
# Build production version
cd medhelp
npm run build

# Deploy dist/ folder to:
# - Vercel
# - Netlify
# - GitHub Pages
# - AWS S3
# - Any static hosting service
```

#### Environment Configuration
Create `.env.production`:
```env
VITE_API_URL=https://api.yourdomain.com
```

---

## 🤝 Contributing

### Development Workflow
1. Create feature branch: `git checkout -b feature/feature-name`
2. Make changes and test locally
3. Commit with descriptive messages: `git commit -m "Add feature description"`
4. Push to GitHub: `git push origin feature/feature-name`
5. Create Pull Request with description

### Code Style
- Python: Follow PEP 8
- TypeScript: Use ESLint + Prettier
- Commit messages: Use conventional commits

### Areas for Contribution
- [ ] Additional medical models
- [ ] Multi-language support
- [ ] Enhanced 3D visualizations
- [ ] Mobile app development
- [ ] Advanced analytics dashboard
- [ ] Integration with healthcare systems (HL7/FHIR)

---

## 📝 License

This project is licensed under the MIT License. See LICENSE file for details.

---

## 📞 Support & Contact

### Issues & Bug Reports
Report bugs via GitHub Issues with:
- Description of problem
- Steps to reproduce
- Expected vs actual behavior
- Screenshots/logs if applicable

### Questions & Discussions
- Check existing documentation
- Review FAQ section
- Post in Discussions section

---

## 🗺️ Roadmap

### Short Term (Q2 2026)
- [ ] Enhanced UI/UX
- [ ] Multi-language support
- [ ] Advanced analytics
- [ ] Performance optimization

### Medium Term (Q3-Q4 2026)
- [ ] Mobile application
- [ ] HL7/FHIR integration
- [ ] Electronic Health Record (EHR) connectivity
- [ ] Advanced biomarker detection

### Long Term (2027+)
- [ ] Federated learning capabilities
- [ ] Real-time collaborative features
- [ ] AI model explainability dashboard
- [ ] Regulatory compliance (SOC 2, HIPAA)

---

## 📚 Resources

### Documentation
- [Flask Documentation](https://flask.palletsprojects.com/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Three.js Documentation](https://threejs.org/docs/)
- [OpenRouter API Docs](https://openrouter.ai/docs)

### Learning Resources
- Medical AI best practices
- Machine learning ethics
- Healthcare compliance (HIPAA)
- Clinical decision support design

---

## ⚠️ Disclaimer

**MEDICAL DISCLAIMER:** This application is designed as a clinical decision support tool and research platform. It should not be used as a replacement for professional medical diagnosis or treatment. Always consult qualified healthcare professionals for medical advice.

---

## 🙏 Acknowledgments

- OpenRouter for providing API access
- OpenAI for GPT-4o vision capabilities
- Three.js community for 3D visualization
- Anthropic for AI ethics guidance

---

**Last Updated:** April 2026  
**Version:** 1.0.0  
**Status:** Active Development

