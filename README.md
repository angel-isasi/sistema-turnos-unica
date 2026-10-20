# Sistema de Turnos UNICA

A queue and appointment management system for university administrative services at Universidad Nacional San Luis Gonzaga (UNICA), built for the Advanced Programming course (2026). I worked as the frontend developer and system architect.

## What it does

- **Students** request a ticket (turno) for a service and see their position in the queue and estimated wait.
- **Staff** call and attend tickets from their service window.
- Reports with service statistics, an audit log of system actions and user management for staff.
- JWT authentication with role-based protected routes, bcrypt-hashed passwords and rate limiting.

## Live demo

👉 https://sistema-turnos-unica.vercel.app

## Tech stack

- **Frontend:** React 19, Vite, React Router, Tailwind CSS v4, shadcn/ui, Lucide icons — deployed on Vercel
- **Backend:** Python, FastAPI, SQLAlchemy, MySQL, PyJWT, bcrypt, SlowAPI — deployed on Railway

## Run locally

Requirements: Node.js, Python 3 and a MySQL database.

**Backend**

```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env            # fill in DATABASE_URL and JWT_SECRET
python seed.py                  # creates initial accounts and services
uvicorn main:app --reload       # http://localhost:8000
```

**Frontend**

```bash
cd frontend
npm install
npm run dev                     # http://localhost:5173
```

The frontend uses `http://localhost:8000` as the API by default (see `frontend/.env.example`).
