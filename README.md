# Thematic-Project-Calorie-Counter-Web-App

# Calorie Tracker Web App

A full-stack web application that allows users to log meals and workouts, track calories consumed and burned, and monitor progress against personal fitness goals. Designed with a mobile-first approach for health-conscious users.

---

## Features

### User Management
- Register, login, and logout
- Secure session token authentication
- Update profile and personal metrics

### Meal Tracking
- Add meals with type (breakfast, lunch, dinner, snack)
- Include calories and consumption time
- View, edit, and delete meals by date

### Workout Tracking
- Log workouts with calories burned (planned feature)
- View total calories burned daily

### Goals and Progress
- Set a daily calorie burn goal
- Compare intake vs. burn and view net progress
- Daily summaries with future support for weekly/monthly trends

---

## Tech Stack

- **Frontend**: Vue 3 (Composition API), Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: SQLite
- **Authentication**: Token-based sessions
- **Validation**: Joi schema validation

---

## Folder Structure
project/
├── backend/
│ ├── controllers/
│ ├── models/
│ ├── routes/
│ └── server.js
├── frontend/
│ ├── components/
│ ├── views/
│ └── store/
├── database/
├── public/
└── README.md

---

## 📦 Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/your-username/calorie-tracker.git
cd calorie-tracker
```

### Backend Setup
```bash
cd backend
npm install
node server.js  # or use nodemon for live reloading
```
(Server runs on: http://localhost:3333)

### Frontend Setup
```
cd frontend
npm install
npm run dev
```
(Frontend runs on: http://localhost:5173)

### API Endpoints (Sample)
```bash
Auth
POST /login

POST /logout

POST /users

Meals
POST /api/activity/meals

GET /api/activity/meals?date=unix_timestamp

DELETE /api/activity/meals/:meal_id

Summary
GET /api/summary/daily?date=unix_timestamp
```

## Notes
Dates are handled in Unix timestamps, adjusted for UK local time.

Form input validates using Joi (e.g., calories must be a number ≥ 0).

Frontend implements debounced search and autocomplete via OpenFoodFacts API.


