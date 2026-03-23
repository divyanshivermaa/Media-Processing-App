# Media Processing App

A full‑stack media utility that generates thumbnails, compresses videos, and extracts audio from public URLs.

## Features
- Thumbnail generation from video URLs
- Video compression
- Audio extraction (MP3)
- FastAPI backend + React (Vite) frontend

## Tech Stack
- **Backend:** FastAPI, Uvicorn, FFmpeg
- **Frontend:** React, Vite

---

## Local Setup

### 1) Backend
```bash
cd backend
python -m venv .venv
# Windows
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m uvicorn main:app --reload --host 127.0.0.1 --port 8001
2) Frontend
bash

cd frontend
npm install
npm run dev -- --host 127.0.0.1 --port 5173
Environment Variables
Backend

ALLOWED_ORIGINS=https://your-frontend-domain
FFMPEG_PATH=C:\path\to\ffmpeg.exe   # optional (local Windows)
Frontend

VITE_API_BASE_URL=https://your-backend-domain/process
Deployment (Railway)
Backend Service
Root directory: backend
Uses Dockerfile (installs FFmpeg automatically)
Frontend Service
Root directory: frontend
Build: npm install && npm run build
Start: npm run preview -- --host 0.0.0.0 --port $PORT
Set env variables:

Backend: ALLOWED_ORIGINS=https://<frontend-domain>
Frontend: VITE_API_BASE_URL=https://<backend-domain>/process
Example URL

https://samplelib.com/lib/preview/mp4/sample-5s.mp4
License
MIT



If you want a shorter README or a more portfolio‑style one, I can rewrite i
