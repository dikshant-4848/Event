## Event Planner - Minimal Fullstack Project
-----------------------------------------

Web application that allows users to create, manage, and RSVP to events. Admins
   can create and modify event details, while users can view available events and respond
   with their attendance status.

------------------------------------------------------------------   
## Contents:
- Backend/: Node.js + Express API using Mongodb Atlas
- Frontend/: Static HTML/CSS/JS frontend to interact with backend.

## Quick start (Windows):
1. Extract ZIP
2. Backend:
   cd backend -> 
   npm install -> 
   cp .env.example .env -> 
  (edit .env if you want)
   node seed.js -> 
   npx nodemon server.js ->
   Server runs at http://localhost:5000

3. Frontend:
   Open frontend/index.html in your browser with localhost

| Role  | Email                                         | Password |
| ----- | --------------------------------------------- | -------- |
| Admin | [admin@example.com](mailto:admin@example.com) | admin123 |
| User  | [user@example.com](mailto:user@example.com)   | user123  |

## Notes:
- RSVP statuses: going, maybe, decline
- Duplicate RSVPs prevented by UNIQUE constraint (userId + eventId)
- You can create more users via signup page
- ER (text):
  Users (id, name, email, password, role)
  Events (id, title, description, date, startTime, endTime, location)
  Rsvps (id, userId -> Users.id, eventId -> Events.id, status)
