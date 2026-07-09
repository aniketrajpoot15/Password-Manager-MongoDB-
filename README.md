# 🔐 PassOP - MongoDB Password Manager

PassOP is a secure, modern, and user-friendly password manager application built using the MERN stack (**React + Vite** for the frontend, **Express** for the backend server, and **MongoDB** for persistent database storage). It allows users to securely save, view, edit, copy, and delete credentials for their online accounts.

---

## 🚀 Features

* **Secure CRUD Operations**: Add, read, update, and delete website credentials directly from/to a MongoDB database.
* **Clipboard Integration**: Easily copy passwords, usernames, or website URLs with a single click.
* **Show/Hide Password Toggle**: Toggle visibility of passwords on the screen for enhanced privacy.
* **Form Validation**: Form-level validation checks (e.g. minimum character lengths) to prevent saving incomplete records.
* **Instant Notifications**: Interactive feedback using custom toast alerts via `react-toastify`.
* **Clean & Modern UI**: Built with Tailwind CSS, featuring dark mode elements and smooth layouts.

---

## 🛠️ Technology Stack

### Frontend
- **Framework**: React 19 (via Vite)
- **Styling**: Tailwind CSS
- **Icons & UI Elements**: Custom SVGs/PNGs
- **Notifications**: `react-toastify`
- **ID Generator**: `uuid`

### Backend
- **Server**: Node.js & Express
- **Database**: MongoDB (via official Driver)
- **CORS Support**: `cors` package
- **Environment variables**: `dotenv`

---

## 📂 Project Structure

```text
Password_Manager_MongoDB/
├── backend/                  # Express server & database logic
│   ├── server.js             # Main server logic & API endpoints
│   ├── package.json          # Node dependencies
│   └── .env                  # Port, DB Name, and MongoDB connection URI
├── src/                      # React frontend
│   ├── components/
│   │   ├── Navbar.jsx        # Top Navigation bar
│   │   ├── Manager.jsx       # Main Dashboard / Logic handler
│   │   └── Footer.jsx        # Footer component
│   ├── App.jsx               # App wrapper
│   ├── main.jsx              # App entry point
│   └── index.css             # Tailwind setup & styling
├── public/                   # Static assets & icons
├── tailwind.config.js        # Tailwind configuration
├── vite.config.js            # Vite configuration
└── package.json              # Frontend dependencies
```

---

## 🔌 API Endpoints

The backend server runs on `http://localhost:3000` and exposes the following RESTful API:

| Method | Endpoint | Description | Request Body |
|---|---|---|---|
| **GET** | `/` | Fetch all saved credentials | None |
| **POST** | `/` | Save a new credential record | `{ id, site, username, password }` |
| **DELETE** | `/` | Delete a credential record | `{ id }` |

---

## ⚙️ Installation & Setup

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) installed and a running **MongoDB** instance (local or MongoDB Atlas).

### 1. Clone the repository
```bash
git clone https://github.com/aniketrajpoot15/Password-Manager-MongoDB-.git
cd Password-Manager-MongoDB-
```

### 2. Configure Environment Variables
Inside the `backend/` directory, create a `.env` file:
```env
MONGO_URI=mongodb://localhost:27017
DB_NAME=passop
```

### 3. Run the Backend
```bash
cd backend
npm install
node server.js
```

### 4. Run the Frontend
Open a new terminal window in the root directory:
```bash
npm install
npm run dev
```

The frontend will run at `http://localhost:5173`. Enjoy managing your passwords securely!
