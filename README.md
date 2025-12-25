# Doc Health — Simple Doctors Marketplace (India)

A minimal React + FastAPI app with WebRTC video calling for online consultations.

## Stack

->Frontend
-React (Vite)
React Router
Axios
Tailwind CSS / CSS
WebRTC APIs
WebSocket / Socket.io Client

->Backend
FastAPI (Python)
REST APIs
WebSockets (for signaling)
JWT Authentication (planned)
Database (Future enhancement):
MongoDB Atlas / PostgreSQL

->WebRTC
Peer-to-peer secure video
FastAPI WebSocket signaling
STUN Server:

## Quickstart

Terminal 1 — Backend:

powershell
cd server
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000 --reload


Terminal 2 — Frontend:

powershell
cd client
npm install
npm run dev

Open http://localhost:5173

## Features
- Browse doctors list (mock data)
- Book appointment (creates a room)
- Join video call using WebRTC (open call link in a second browser/device)
- Real-time consultation room creation using WebSockets
- Secure peer-to-peer video and audio communication
- Unique room ID generation for each appointment
- Doctor availability status (Online / Offline)
- Patient and doctor name display inside call screen
- Auto-cleanup of expired or completed appointments
- Responsive UI (works on mobile and desktop)
- Simple and beginner-friendly architecture for learning/demo


## Notes
- Storage is in-memory for demo—appointments reset on backend restart
- CORS is configured for Vite dev server
- STUN server: Google public (for NAT traversal)

## Project Structure

doc-health/
  server/         # FastAPI backend
    main.py
    requirements.txt
  client/         # React frontend (Vite)
    index.html
    vite.config.js
    package.json
    src/
      App.jsx
      main.jsx
      api.js
      pages/
        Doctors.jsx
        Book.jsx
        Appointments.jsx
        VideoCall.jsx
      styles.css

