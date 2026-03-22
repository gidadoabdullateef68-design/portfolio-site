# 💸 SpendWise — Personal Finance Tracker

> A full-stack web app to track income, expenses, and budgets in real time. Built with a REST API backend and a responsive React dashboard.

![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?style=flat&logo=node.js&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?style=flat&logo=postgresql&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

## 📸 Preview

> _Dashboard screenshot or GIF goes here — even a placeholder image works_

---

## ✨ Features

- 🔐 JWT-based authentication (register, login, logout)
- 📊 Real-time dashboard with income vs. expense charts
- 🗂️ Category-based transaction management
- 📅 Filter transactions by date range or category
- 📤 Export data as CSV
- 🌙 Light/dark mode toggle
- 📱 Fully responsive on mobile

---

## 🛠️ Tech Stack

**Backend**

- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/) — REST API
- [PostgreSQL](https://www.postgresql.org/) — relational database
- [Prisma](https://www.prisma.io/) — ORM for database queries
- [JWT](https://jwt.io/) — stateless authentication
- [bcrypt](https://www.npmjs.com/package/bcrypt) — password hashing

**Frontend**

- [React 18](https://react.dev/) + [Vite](https://vitejs.dev/)
- [Tailwind CSS](https://tailwindcss.com/) — utility-first styling
- [Recharts](https://recharts.org/) — data visualisation
- [React Query](https://tanstack.com/query) — server state management
- [Axios](https://axios-http.com/) — HTTP client

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+
- PostgreSQL 15+
- npm or yarn

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/spendwise.git
cd spendwise
```

### 2. Set up the backend

```bash
cd server
npm install
```

Create a `.env` file in the `server/` directory:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/spendwise"
JWT_SECRET="your_jwt_secret_here"
PORT=5000
```

Run database migrations:

```bash
npx prisma migrate dev --name init
```

Start the server:

```bash
npm run dev
```

### 3. Set up the frontend

```bash
cd ../client
npm install
npm run dev
```

The app will be live at `http://localhost:5173`

---

## 📁 Project Structure

```
spendwise/
├── client/                  # React frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Route-level pages
│   │   ├── hooks/           # Custom React hooks
│   │   ├── services/        # API call functions
│   │   └── main.jsx
│   └── vite.config.js
│
├── server/                  # Express backend
│   ├── src/
│   │   ├── controllers/     # Route handlers
│   │   ├── middleware/      # Auth, error handling
│   │   ├── routes/          # API route definitions
│   │   └── index.js
│   ├── prisma/
│   │   └── schema.prisma    # Database schema
│   └── package.json
│
└── README.md
```

---

## 🔌 API Endpoints

| Method | Endpoint                | Description               | Auth |
| ------ | ----------------------- | ------------------------- | ---- |
| POST   | `/api/auth/register`    | Create new account        | ❌   |
| POST   | `/api/auth/login`       | Login and receive JWT     | ❌   |
| GET    | `/api/transactions`     | Get all transactions      | ✅   |
| POST   | `/api/transactions`     | Add new transaction       | ✅   |
| PUT    | `/api/transactions/:id` | Update transaction        | ✅   |
| DELETE | `/api/transactions/:id` | Delete transaction        | ✅   |
| GET    | `/api/summary`          | Get income/expense totals | ✅   |

---

## 🧪 Running Tests

```bash
# Backend unit tests
cd server
npm run test

# Frontend component tests
cd client
npm run test
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push to your branch: `git push origin feat/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## 👤 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [linkedin.com/in/yourname](https://linkedin.com/in/yourname)
