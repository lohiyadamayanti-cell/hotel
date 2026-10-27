#HotelPro - Full-Stack Hotel Management & Booking Solution

HotelPro is a scalable, role-based hotel reservation and management system built on the **MERN** stack (MongoDB, Express.js, React.js, Node.js).

---

## 🚀 Tech Stack

- **Frontend:** React.js, Bootstrap / Modern CSS, Axios, React Router
- **Backend:** Node.js, Express.js REST API
- **Database:** MongoDB Atlas with Mongoose ORM
- **Authentication:** JSON Web Tokens (JWT) & bcrypt.js password hashing

---

## 📁 Project Structure

```text
hotelpro/
├── client/          # Frontend React Application
├── server/          # Backend Express & MongoDB API
│   ├── config/      # Database & configuration
│   ├── controllers/ # Route controller logic
│   ├── middleware/  # Auth guards & error handlers
│   ├── models/      # Mongoose database models
│   ├── routes/      # Express API routes
│   └── utils/       # Token & utility functions
└── README.md
```

---

## 🛠️ Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Ayushgupta-lab/hotel.git
cd hotel
```

### 2. Backend Setup
```bash
cd server
npm install
```
Create a `.env` file in the `server` directory (reference `.env.example`):
```env
PORT=5000
NODE_ENV=development
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
CLIENT_URL=http://localhost:5173
```

Start the backend:
```bash
npm run dev
```

Server will run on: `http://localhost:5000`
Health check: `http://localhost:5000/api/health`

- `200` + `"database": "connected"` once MongoDB is reachable.
- `503` + `"database": "disconnected"` while it is not — the API keeps serving instead of crashing, and retries the connection in the background.

### 3. Run the tests
```bash
cd server
npm test
```
This boots an in-memory MongoDB, starts the API against it and asserts the health check, root route and 404 handler all behave.

