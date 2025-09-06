# 🛒 GreenCart Backend API

A robust **Node.js backend API** for the GreenCart e-commerce platform, built with **Express.js** and **MongoDB**.

---

## 🚀 Features

### 🔐 Authentication & Authorization

* ✅ **JWT Authentication** – Secure token-based authentication
* ✅ **User Registration/Login** – Email and password login
* ✅ **Seller Authentication** – Separate seller login system
* ✅ **Protected Routes** – Middleware-based route protection
* ✅ **HTTP-only Cookies** – Secure token storage

### 📦 Product Management

* ✅ **CRUD Operations** – Create, read, update, delete products
* ✅ **Image Upload** – Cloudinary integration for product images
* ✅ **Category Management** – Organize products by categories
* ✅ **Inventory Tracking** – Manage stock and availability
* ✅ **Search & Filter** – Powerful product search and filtering

### 🛍️ Shopping Cart & Orders

* ✅ **Cart Management** – Add, remove, update cart items
* ✅ **Order Processing** – Create and manage orders
* ✅ **Address Management** – Support for multiple shipping addresses
* ✅ **Payment Integration** – Stripe payment gateway
* ✅ **Order Tracking** – Manage and update order status

### 📊 Data Management

* ✅ **MongoDB Integration** – NoSQL database with Mongoose
* ✅ **Data Validation** – Input validation and sanitization
* ✅ **Error Handling** – Comprehensive error management
* ✅ **CORS Configuration** – Cross-origin resource sharing

---

## 📂 Project Structure

```
server/
├── configs/              # Configuration files
│   ├── db.js             # MongoDB connection
│   ├── cloudinary.js     # Cloudinary setup
│   └── multer.js         # File upload config
├── controllers/          # Business logic
│   ├── userController.js
│   ├── sellerController.js
│   ├── productController.js
│   ├── cartController.js
│   ├── orderController.js
│   └── addressController.js
├── middlewares/          # Custom middleware
│   ├── authUser.js
│   └── authSeller.js
├── models/               # Database schemas
│   ├── User.js
│   ├── Product.js
│   ├── Order.js
│   └── Address.js
├── routes/               # API routes
│   ├── userRoute.js
│   ├── sellerRoute.js
│   ├── productRoute.js
│   ├── cartRoute.js
│   ├── orderRoute.js
│   └── addressRoute.js
├── server.js             # Main server file
├── package.json
└── vercel.json
```

---

## 🛠️ Tech Stack

* **Node.js** – Runtime environment
* **Express.js 5.1.0** – Web framework
* **MongoDB** – NoSQL database
* **Mongoose 8.18.0** – ODM for MongoDB
* **JWT 9.0.2** – Authentication
* **Stripe 18.4.0** – Payment integration
* **Cloudinary 2.7.0** – Image storage
* **Multer 2.0.2** – File upload
* **Bcryptjs 3.0.2** – Password hashing
* **CORS 2.8.5** – Cross-origin requests

---

## ⚡ Getting Started

### ✅ Prerequisites

* Node.js **v16+**
* MongoDB Database
* Cloudinary Account
* Stripe Account

### 📥 Installation

1. **Navigate to server directory**

   ```bash
   cd server
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Setup**
   Create `.env` file in `server/`:

   ```env
   PORT=4000
   MONGODB_URI=mongodb://localhost:27017/greencart
   JWT_SECRET=your_super_secret_jwt_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key
   STRIPE_WEBHOOK_SECRET=whsec_your_webhook_secret
   NODE_ENV=development
   ```

4. **Start the server**

   ```bash
   # Development mode with nodemon
   npm run server

   # Production mode
   npm start
   ```

5. Server will run on 👉 `http://localhost:4000`

---

## 📊 API Documentation

### 🌍 Base URL

```
http://localhost:4000/api
```

### 🔑 Authentication Endpoints

#### ➡️ User Registration

```http
POST /api/user/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

#### ➡️ User Login

```http
POST /api/user/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "password123"
}
```

---

## 📌 Deployment

This project is ready to be deployed on **Vercel** using the provided `vercel.json` configuration.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to fork and submit PRs.

---

## 📜 License

This project is licensed under the **MIT License**.

---
