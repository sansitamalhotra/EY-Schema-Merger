🌟 Overview

When two banks merge, data chaos follows — each system has its own schema, column names, and formats.
Schema Sync is your AI-powered copilot that maps, merges, and validates financial datasets across institutions — producing a unified schema and audit trail in minutes, not days.

It’s like GitHub Copilot — but for data mapping and schema reconciliation.

🎯 Key Features

🤖 AI Schema Matching — Embedding-based NLP (OpenAI/SBERT) for semantic column alignment

📂 Multi-Format Uploads — Supports CSV, Excel (.xlsx, .xls), and JSON

🧩 Visual Mapping Workspace — Side-by-side schemas with drag-to-match & confidence scores

📈 Analytics Dashboard — Power BI–style insights: completeness, overlaps, KPIs

⚙️ Conflict Resolver — Detects mismatched fields, missing data, format inconsistencies

🧾 Report Generation — Exports Excel & PDF with mappings and confidence metrics

🛡️ Secure Local Processing — All data handled locally with transparency

🎨 Elegant UI — Built with Next.js, Tailwind, and shadcn/ui

🏗️ Architecture
🧠 Backend (FastAPI + Python)

Schema Parser — Reads and normalizes schema structure

AI Matcher — Uses embeddings for semantic field pairing

Merge Engine — Combines datasets into a unified schema

Analytics Service — Computes completeness & conflict metrics

Report Generator — Exports Excel/PDF with audit trail

Storage Layer — Organizes files per institution

💻 Frontend (Next.js + React + Tailwind)

Guided Workflow — Upload → Map → Merge → Analyze → Export

Drag-and-Drop Uploads — Containers for Bank A & Bank B datasets

Dynamic Mapping View — Real-time AI confidence scores

Interactive Dashboard — KPIs, charts, and data completeness metrics

Responsive Design — Optimized for all devices

🚀 Quick Start
🧰 Prerequisites

Python 3.11+

Node.js 18+

An OpenAI API Key

⚙️ 1. Clone the Repository
git clone https://github.com/your-username/schema-sync.git
cd schema-sync

📦 2. Backend Setup

There’s no requirements.txt, so install dependencies manually.

cd backend
pip install fastapi uvicorn openai pandas python-multipart


Then start the backend:

uvicorn main:app --reload --port 8000

💻 3. Frontend Setup
cd ../frontend
npm install
npm run dev

🌐 4. Access the App
Service	URL
Frontend	http://localhost:3000

Backend	http://localhost:8000

Health Check	http://localhost:8000/health
🧩 5. Configure Environment Variables

Create a .env file in /backend and add:

OPENAI_API_KEY=your_openai_api_key_here
FASTAPI_PORT=8000

🧪 Usage Guide
Step 1 – Upload Schemas

Upload Bank A and Bank B schema files

Schema Sync auto-detects columns, data types, and formats

Step 2 – AI Mapping

View AI-suggested pairings with confidence scores

Drag and adjust or approve mappings manually

Step 3 – Merge Preview

Review unified dataset

See live stats: records merged, overlap %, unresolved fields

Step 4 – Analytics Dashboard

Completeness Score gauge

Conflict & overlap summaries

Visual charts for insight into integration quality

Step 5 – Export

Download unified dataset (Excel/CSV)

Generate PDF Integration Report with mappings, KPIs, and audit trail

🔧 API Endpoints
Method	Endpoint	Description
GET	/health	Check server status
POST	/schemas/parse	Parse uploaded schema
POST	/upload	Upload data files
POST	/process/ai-map	Trigger AI schema matching
GET	/download/	Download unified dataset
POST	/cleanup	Remove temporary data
🧱 Project Structure
schema-sync/
├── backend/
│   ├── main.py
│   ├── matcher.py
│   ├── merger.py
│   ├── parser.py
│   └── uploaded_files/
│       ├── bankA/
│       └── bankB/
├── frontend/
│   ├── pages/
│   ├── components/
│   ├── public/images/
│   └── styles/
├── reports/
└── README.md

🔒 Security & Privacy

Local-Only Processing — No cloud data transfer

Strict Validation — File type & size checks

Auto Cleanup — Deletes temp files post-export

Environment Security — API key stored in .env

Sanitized Logs — No sensitive data retained

🧰 Troubleshooting
Issue	Fix
Backend fails to start	Reinstall deps, confirm Python 3.11+
Frontend blank page	Clear cache or rerun npm run dev
AI mapping not working	Check OPENAI_API_KEY validity
File not recognized	Use CSV/Excel under 50 MB
🤝 Contributing

Fork this repository

Create a new branch → git checkout -b feature/your-feature

Commit your changes → git commit -m "Add new feature"

Push → git push origin feature/your-feature

Open a Pull Request
Schema Sync — Bridging data across banks with AI and trust.
Made with ❤️ at Hack the Valley X 2025

Schema Sync — Bridging data across banks with AI and trust.
Made with ❤️ at Hack the Valley X 2025
