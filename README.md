# 📝 MERN Blog App

A full-stack blog application built with MongoDB, Express.js, React, and Node.js (MERN stack). This project allows users to create, edit, and delete blog posts, manage categories, comment on posts, and upload images.

## 🔍 Features

- ✅ User authentication (JWT-based)
- ✅ Create, edit, delete blog posts
- ✅ Category management
- ✅ Image upload (local or Cloudinary)
- ✅ Comment system with deletion
- ✅ Responsive UI with Tailwind CSS
- ✅ Post search by title
- ✅ Toast notifications for feedback
- ✅ Pagination-ready structure

---

## 📁 Project Structure
```
mern-blog/
├── client/ # React Frontend (Vite)
│ ├── pages/
│ ├── components/
│ ├── context/
│ └── services/
├── server/ # Express Backend
│ ├── models/
│ ├── routes/
│ ├── controllers/
│ └── middleware/
└── uploads/ # Uploaded images (if local)
```
```
mern-blog/
├── client/                 # React front-end
│   ├── public/             # Static files
│   ├── src/                # React source code
│   │   ├── assets/         # Assets
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── services/       # API services
│   │   ├── context/        # React context providers
│   │   └── App.jsx         # Main application component
│   └── package.json        # Client dependencies
├── server/                 # Express.js back-end
│   ├── controllers/        # Route controllers
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── middleware/         # Custom middleware
│   ├── uploads/            # Local Image Uploads
│   ├── server.js           # Main server file
│   └── package.json        # Server dependencies
└── README.md               # Project documentation
```
---
## ⚙️ Tech Stack

**Frontend:** React + Vite + Tailwind CSS  
**Backend:** Node.js + Express + MongoDB + Mongoose  
**Auth:** JWT tokens  
**Upload:** Multer  

---

## 🚀 Getting Started

### 🧩 Prerequisites

- Node.js
- MongoDB (local or cloud)

---

### 📦 Backend Setup

```
cd server
npm install
cp .env.example .env
# Then set your MongoDB and JWT_SECRET
npm run dev

cd client
npm install
cp .env.example .env
# Set VITE_API_URL (e.g., http://localhost:5000/api)
npm run dev
```
# 🧪 API Documentation
## 🔐 Auth
#### Endpoint	Method	Description
- /api/auth/register	POST	Register a new user
- /api/auth/login	POST	Login and receive token
## 📘 Posts
#### Endpoint	Method	Description
- /api/posts	GET	Get all posts 
- /api/posts/:id	GET	Get a single post
- /api/posts	POST	Create post (auth required)
- /api/posts/:id	PUT	Update post (auth + owner)
- /api/posts/:id	DELETE	Delete post (auth + owner)
## 📁 Categories
#### Endpoint	Method	Description
- /api/categories	GET	Get all categories
- /api/categories	POST	Create new category
## 💬 Comments
#### Endpoint	Method	Description
- /api/comments/:postId	GET	Get comments for a post
- /api/comments	POST	Add comment (auth required)
- /api/comments/:id	DELETE	Delete comment (auth + owner)

## 📷 Image Upload

#### By default, uses multer to store images in /uploads


# 🙌 Contributing

- You are welcomed To contribute:

- Fork the repo

- Create a branch (git checkout -b feature-name)

- Commit your changes

- Open a pull request

📄 License