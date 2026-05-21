<div align="center">

# 🚗 MARQUE DESIGN

### Luxury Car Customization Platform

![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-5.x-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-ISC-blue?style=for-the-badge)

*A premium, dark-themed web application for luxury car customization, featuring role-based authentication, real-time configurator, and admin management.*

</div>

---

## ✨ Features

- 🔐 **Secure Authentication** — Email/password login, Google OAuth 2.0, JWT sessions
- 🚘 **Live Car Configurator** — Real-time modification builder with price calculator
- 👤 **User Dashboard** — Profile management, order history, saved favorites
- 🛠️ **Admin Panel** — Inventory management, order status updates, user management
- 📧 **Email Notifications** — Transactional emails via Nodemailer + Gmail SMTP
- 🌙 **Premium Dark UI** — Glassmorphism design with neon accents and micro-animations
- 📱 **Responsive** — Fully mobile-friendly layout

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | Node.js, Express 5 |
| **Database** | MongoDB Atlas (Mongoose ODM) |
| **Auth** | Passport.js, bcryptjs, JWT, Google OAuth 2.0 |
| **Email** | Nodemailer (Gmail SMTP) |
| **Frontend** | Vanilla HTML5, CSS3, JavaScript (ES6+) |
| **Sessions** | express-session, cookie-parser |

---

## 📂 Project Structure

```
marque-design/
├── public/                  # Frontend (served statically)
│   ├── index.html           # Landing page
│   ├── login.html           # Auth page
│   ├── customize.html       # Car configurator
│   ├── profile.html         # User dashboard
│   ├── admin.html           # Admin panel
│   ├── css/                 # Stylesheets
│   │   ├── styles.css       # Global styles
│   │   ├── navbar.css       # Navigation styles
│   │   ├── preloader.css    # Loading animation
│   │   └── profile.css      # Dashboard styles
│   ├── js/                  # Client-side scripts
│   │   ├── common.js        # Shared utilities & API helpers
│   │   ├── auth.js          # Authentication logic
│   │   ├── customize.js     # Configurator logic
│   │   ├── profile.js       # Dashboard logic
│   │   ├── admin.js         # Admin panel logic
│   │   ├── navbar.js        # Navigation logic
│   │   ├── preloader.js     # Loading screen
│   │   ├── checkout.js      # Checkout flow
│   │   └── car-selector.js  # Car selection logic
│   └── images/              # Static assets
└── src/                     # Backend source
    ├── server.js            # Express app entry point
    ├── database.js          # MongoDB connection
    ├── config/
    │   └── passport.js      # Passport OAuth strategies
    ├── middleware/
    │   └── auth.js          # Auth middleware (JWT + session guard)
    ├── models/
    │   └── User.js          # Mongoose User schema
    ├── routes/
    │   └── auth.js          # Auth API routes
    └── services/
        └── emailService.js  # Email sending service
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js 18+](https://nodejs.org/)
- [MongoDB Atlas](https://www.mongodb.com/atlas) account
- Gmail account with [App Password](https://myaccount.google.com/apppasswords) enabled
- Google Cloud project with OAuth 2.0 credentials

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/marque-design.git
cd marque-design

# 2. Install dependencies
npm install

# 3. Configure environment variables
cp .env.example .env
# Edit .env with your real credentials

# 4. Start the development server
npm run dev
```

Open **http://localhost:3000** in your browser.

---

## ⚙️ Environment Variables

Copy `.env.example` to `.env` and fill in each value:

| Variable | Description |
|---|---|
| `PORT` | Server port (default: 3000) |
| `MONGODB_URI` | MongoDB Atlas connection string |
| `SESSION_SECRET` | Long random string for session signing |
| `EMAIL_USER` | Gmail address for sending emails |
| `EMAIL_PASSWORD` | Gmail App Password (not your account password) |
| `JWT_SECRET` | Long random string for JWT signing |
| `GOOGLE_CLIENT_ID` | Google OAuth client ID |
| `GOOGLE_CLIENT_SECRET` | Google OAuth client secret |
| `ADMIN_PASSWORD` | Admin account password |

> ⚠️ **Never commit your `.env` file.** It is already listed in `.gitignore`.

---

## 📜 Available Scripts

| Script | Command | Description |
|---|---|---|
| Development | `npm run dev` | Start server with Node.js |
| Production | `npm start` | Start in production mode |
| Setup | `npm run setup` | Install deps + setup reminder |

---

## 🔒 Security Notes

- Passwords are hashed with **bcryptjs** (12 rounds)
- Sessions are signed with a secret key
- Rate limiting is applied to all auth endpoints
- CORS is configured to restrict origins
- `.env` and credential files are excluded from version control

---

## 📄 License

This project is licensed under the **ISC License**.

---

<div align="center">
  Built with ❤️ — GHOSTINMODEL

</div>
