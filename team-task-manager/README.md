# TaskFlow — Team Task Manager

A full-stack collaborative project & task management app with role-based access control.

## Features
- **Authentication** — JWT-based signup/login
- **Projects** — Create, manage, and delete projects[cite: 1]
- **Team Management** — Invite members with Admin/Member roles[cite: 1]
- **Tasks** — Create tasks with status, priority, due date, and assignee[cite: 1]
- **Kanban Board** — Visual To Do / In Progress / Done columns[cite: 1]
- **Dashboard** — Personal task overview and project stats[cite: 1]

## Tech Stack
| Layer | Technology |
|-------|-----------|
| Frontend | React 18, React Router v6[cite: 1]
| Backend | Node.js, Express[cite: 1]
| Database | PostgreSQL (Hosted on Render)[cite: 1]
| Auth | JWT + bcrypt[cite: 1]
| Deployment | Render[cite: 1]

---

## Live Links
- **Live Application**: https://team-task-manager-2-vtw6.onrender.com
- **GitHub Repository**: https://github.com/rudrakulkarni04/team-task-manager

---

## Local Development
### Prerequisites
- Node.js 18+[cite: 1]
- PostgreSQL[cite: 1]

### Backend Setup
1. cd backend
2. npm install
3. cp .env.example .env
4. npm run dev[cite: 1]

### Frontend Setup
1. cd frontend
2. npm install
3. cp .env.example .env
4. npm start[cite: 1]

---

## Deployment Information
This project is deployed using **Render**.
- **Backend**: Deployed as a Web Service connected to a Managed PostgreSQL instance.
- **Frontend**: Deployed as a Static Site for optimized production performance.
- **Environment Management**: Connected via REACT_APP_API_URL environment variables.

---

## API Endpoints

### Auth
| Method | Route | Access |
|--------|-------|--------|
| POST | /api/auth/register | Public[cite: 1]
| POST | /api/auth/login | Public[cite: 1]
| GET | /api/auth/me | Private[cite: 1]

### Projects
| Method | Route | Access |
|--------|-------|--------|
| GET | /api/projects | Private[cite: 1]
| POST | /api/projects | Private[cite: 1]
| PUT | /api/projects/:id | Admin[cite: 1]
| DELETE | /api/projects/:id | Owner[cite: 1]

### Tasks
| Method | Route | Access |
|--------|-------|--------|
| GET | /api/projects/:id/tasks | Member+[cite: 1]
| POST | /api/projects/:id/tasks | Member+[cite: 1]
| PUT | /api/projects/:id/tasks/:taskId | Member+[cite: 1]

---

## Role-Based Access Control (RBAC)
| Action | Member | Admin |
|--------|--------|-------|
| View project | ✓ | ✓[cite: 1]
| Create tasks | ✓ | ✓[cite: 1]
| Delete tasks | ✗ | ✓[cite: 1]
| Delete project | ✗ | Owner only[cite: 1]
