# 🌱 Ingrow

> A full-stack social media web application inspired by Instagram — built with React, TypeScript, Node.js, Express, and MongoDB.

![License](https://img.shields.io/badge/license-MIT-green)
![Node](https://img.shields.io/badge/node-%3E%3D18.x-brightgreen)
![React](https://img.shields.io/badge/react-18.2-blue)
![MongoDB](https://img.shields.io/badge/database-MongoDB-green)

---

## ✨ Features

- 🔐 **Authentication** — Secure user registration & login with JWT + HTTP-only cookies
- 🖼️ **Image Uploads** — Upload posts with images stored via Cloudinary
- 📰 **Feed** — Dynamic home feed showing posts from users you follow
- 👤 **User Profiles** — View and edit your profile
- ❤️ **Likes & Comments** — Interact with posts in real time
- 📱 **Responsive UI** — Mobile-friendly design with Tailwind CSS

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React 18 + TypeScript | UI Framework |
| Vite | Build tool & dev server |
| Tailwind CSS | Styling |
| React Router v6 | Client-side routing |
| Zustand | Global state management |
| Axios | HTTP client |

### Backend
| Technology | Purpose |
|---|---|
| Node.js + Express | REST API server |
| MongoDB + Mongoose | Database & ODM |
| JSON Web Tokens (JWT) | Authentication |
| Bcrypt.js | Password hashing |
| Cloudinary + Multer | Image storage & uploads |
| Cookie-Parser | Cookie handling |
| Morgan | HTTP request logging |

---

## 📁 Project Structure

```
ingrow/
├── client/                  # React + TypeScript frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Route-level pages
│   │   │   ├── Home.tsx
│   │   │   └── auth/        # Login & Register pages
│   │   ├── hooks/           # Custom React hooks
│   │   ├── store/           # Zustand global state
│   │   └── App.tsx
│   ├── tailwind.config.js
│   └── package.json
│
└── server/                  # Node.js + Express backend
    ├── controllers/         # Route logic
    ├── models/              # Mongoose models (User, Post)
    ├── routes/              # API routes
    │   ├── authRoutes.js
    │   └── postRoutes.js
    ├── server.js            # App entry point
    └── package.json
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- [MongoDB](https://www.mongodb.com/) (local or Atlas cloud)
- [Cloudinary](https://cloudinary.com/) account (for image uploads)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ingrow.git
cd ingrow
```

### 2. Setup the Backend

```bash
cd server
npm install
```

Create a `.env` file inside the `server/` folder:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
NODE_ENV=development
```

Start the backend server:

```bash
npm run dev
```

The API will be running at `http://localhost:5000`

### 3. Setup the Frontend

```bash
cd ../client
npm install
npm run dev
```

The frontend will be running at `http://localhost:5173`

---

## 📡 API Endpoints

### Auth Routes — `/api/auth`
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/register` | Register a new user |
| POST | `/login` | Login and receive JWT cookie |
| POST | `/logout` | Logout and clear cookie |

### Post Routes — `/api/posts`
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Get all posts (feed) |
| POST | `/` | Create a new post |
| DELETE | `/:id` | Delete a post |
| PUT | `/:id/like` | Like / unlike a post |

---

## 🔒 Environment Variables

> ⚠️ **Never commit your `.env` file to GitHub.** It is already listed in `.gitignore`.

| Variable | Description |
|---|---|
| `PORT` | Server port (default: 5000) |
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret key for signing JWTs |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |
| `NODE_ENV` | `development` or `production` |

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the project
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

Made with ❤️ by **ADITYA DUBEY**

---

> ⭐ If you found this project useful, please consider giving it a star on GitHub!
