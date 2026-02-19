# Academix

A full-stack **university dashboard and classroom management** platform. Admins, teachers, and students use a single app with role-appropriate views: dashboard analytics, subjects, departments, faculty, classes, and code-based enrollment (invite codes).

## Stack

| Layer    | Tech |
|----------|------|
| Frontend | React, TypeScript, Refine, shadcn/ui, Tailwind, Better Auth (client), Cloudinary |
| Backend  | Node.js, Express, Better Auth, Drizzle ORM |
| Database | PostgreSQL (Neon) |

## Repo structure

- **`classroom-frontend/`** — React (Vite) SPA; runs on port 5173 by default.
- **`classroom-backend/`** — Express API and Better Auth; runs on port 8000.

## Quick start

1. **Backend**

   ```bash
   cd classroom-backend
   cp .env.example .env   # or create .env with DATABASE_URL, FRONTEND_URL, BETTER_AUTH_SECRET, etc.
   npm install
   npm run db:migrate     # create tables
   npm run db:seed        # optional: seed data
   npm run dev
   ```

2. **Frontend**

   ```bash
   cd classroom-frontend
   npm install
   # Create .env with VITE_BACKEND_BASE_URL, Cloudinary vars
   npm run dev
   ```

3. Open **http://localhost:5173** and register or log in.

## Features

- **Auth:** Email/password sign-up and sign-in (Better Auth).
- **Roles:** Admin, Teacher, Student with different capabilities.
- **Dashboard:** Overview of users, subjects, departments, classes.
- **Subjects & departments:** CRUD and detail views.
- **Faculty:** List and profile views.
- **Classes:** Create classes, assign teachers, generate invite codes.
- **Enrollments:** Students join by selecting a class or entering an invite code.
- **Media:** Profile and class banner uploads via Cloudinary (unsigned preset).

## License

MIT
