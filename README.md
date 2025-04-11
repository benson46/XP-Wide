# 🛒 XPWide – Full-Stack E-Commerce Platform (MERN)

🔗 **XPWide Live Site:** [Xpwide-live](https://xpwide.tech/)  
📦 **Frontend Repo:** [Xpwide-Client](https://github.com/benson46/Xpwide-Client)  
🛠 **Backend Repo:** [Xpwide-Server](https://github.com/benson46/Xpwide-Server)

**Frontend:** Vercel | **Backend:** AWS EC2  

XPWide is a robust, full-featured MERN (MongoDB, Express.js, React, Node.js) e-commerce platform with full shopping functionality including user and admin management, order tracking, secure authentication, and payment integration.

---

## ✨ Features

### 👤 User Side
- Browse and search products
- Add to cart and wishlist
- Secure user authentication (JWT)
- View order history and manage profile
- Multiple payment options (Razorpay, Wallet, COD)

### 🛠️ Admin Dashboard
- Product management (Add, Edit, Delete)
- Order tracking and management
- User controls (View, Block)
- Basic analytics and dashboard insights

---

## 🔐 Backend Highlights

- **Framework:** Node.js + Express.js
- **Database:** MongoDB (with Mongoose)
- **Authentication:** JWT-based (Access + Refresh Tokens)
- **Cache:** Redis for performance optimization
- **Image Storage:** Cloudinary for secure and optimized image handling
- **Architecture:** MVC pattern for clean code structure

---

## 💳 Payment Integration

- **Razorpay:** Integrated secure payment gateway
- **Custom Wallet System:** Users can use internal balance
- **COD:** Cash on Delivery support

---

## 🚀 Deployment

- **Frontend:** Vercel
- **Backend:** AWS EC2
- **Database:** MongoDB Atlas (Cloud DB)
- **Image Hosting:** Cloudinary

---

## 📦 Tech Stack

| Frontend        | Backend           | Database     | Others                  |
|-----------------|-------------------|--------------|--------------------------|
| React.js        | Node.js + Express | MongoDB      | Cloudinary (images)     |
| Redux Toolkit   | JWT + Redis       | Redis (cache)| Razorpay (payments)     |
| Axios           | MVC Architecture  | MongoDB Atlas| AWS EC2, Vercel (hosting)|

---


## Install Dependencies

```
gitclone https://github.com/benson46/XP-Wide.git
```
 - Client
```
cd Xpwide-Client
npm install
npm run dev
```
- Server:

```

cd Xpwide-Server
npm install
npm run start

```
🔐 Add .env files for both client and server with relevant API keys, secrets, and URLs.


# 🔐 Backend Environment Variables (.env)
Create a .env file in your Xpwide-Server/ directory with the following keys:

change things with yours
``` 
PORT=5000
MONGO_URI=YOUR_ATLAS

NODE_ENV=development

# Redis Configuration
REDIS_HOST=YOUR_REDIS
REDIS_PASSWORD=YOUR_REDIS_PASSWORD
REDIS_PORT=YOUR_REDIS_PORT

# JWT Config
ACCESS_TOKEN_LIFETIME=15m
ACCESS_TOKEN_SECRET=your_access_token_secret
REFRESH_TOKEN_LIFETIME=7d
REFRESH_TOKEN_SECRET=your_refresh_token_secret

JWT_SECRET=secret
JWT_TIMEOUT=12h

# CORS Allowed Origins
CORS_CLIENT_SIDE=https://www.yourdomain.com
CORS_CLIENT_SIDE1=https://yourdomain.com
CORS_CLIENT_SIDE2=http://localhost:5173

# Cloudinary Config
CLOUDINARY_URL=YOUR_CLOUDINARY_API_LINK
CLOUDINARY_CLOUD_NAME=YOUR_CLOUDINARY_NAME
CLOUDINARY_API_KEY=YOUR_CLOUDINARY_API_KEY
CLOUDINARY_API_SECRET=YOUR_CLOUDINARY_API_SECRET

# Email (Nodemailer)
NODEMAILER_EMAIL=YOUR_EMAIL
NODEMAILER_PASS=YOUR_APP_PASSWORD
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587

# Google OAuth
GOOGLE_CLIENT_ID=YOUR_GOOGLE_CLIENT_ID
GOOGLE_CLIENT_SECRET=YOUR_GOOGLE_CLIENT_SECRET
```

⚠️ Never commit this .env file to version control. Add it to .gitignore to keep your secrets safe.

# 🌐 Frontend Environment Variables (.env)
Create a .env file in your Xpwide-Client/ root directory with the following values:

```
VITE_USER_API_BASE_URL=http://localhost:5000/api/user
VITE_ADMIN_API_BASE_URL=http://localhost:5000/api/admin
VITE_GOOGLE_USER_API_BASE_URL=http://localhost:5000/api/google

VITE_APP_TITLE=YOUR_APP_TITLE

VITE_GOOGLE_CLIENT_ID=YOUR_GOOGLE_CLIENTID
VITE_RAZORPAY_KEY=YOUR_RAZORPAY_KEY

```

✅ Make sure you're using Vite syntax (VITE_) for all environment variables — required for the frontend to pick them up correctly.