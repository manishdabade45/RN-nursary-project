# 🌿 R.N. Agritech Services

> **Professional Landscape Gardening & Agricultural Consultancy Platform**

A full-stack e-commerce and services website for **R.N. Agritech Services**, a leading provider of landscape gardening, agricultural consultancy, and pest control services based in Pune, Maharashtra, India.

🔗 **Live Demo:** [https://rn-nursary-project.vercel.app](https://rn-nursary-project.vercel.app/index.html)

🔗 **Backend API:** [https://rn-nursary-project.onrender.com](https://rn-nursary-project.onrender.com/api/health)

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Deployment](#deployment)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🏡 About

R.N. Agritech Services is a comprehensive web platform that showcases landscaping services and allows customers to:

- Browse and purchase plants, trees, and horticultural materials
- Explore professional landscaping and agricultural consultancy services
- Manage their cart and place orders online
- Contact the business for custom project inquiries

---

## ✨ Features

### 🎨 Frontend
- **Responsive Design** — Fully responsive across all devices (mobile, tablet, desktop)
- **Dark/Light Theme** — Toggle between dark and light modes
- **Interactive Plant Store** — Browse, search, and filter plants with an add-to-cart system
- **User Authentication** — Login and registration with JWT-based auth
- **Shopping Cart** — Persistent cart with quantity management
- **Order Management** — Place orders and view order history
- **Contact Form** — Inquiry form with service selection and character counter
- **Blog Section** — Informational gardening blog posts
- **Admin Dashboard** — Manage products, orders, and users
- **Smooth Animations** — Scroll animations and hover effects for a premium feel

### 🔧 Backend (REST API)
- **JWT Authentication** — Secure user registration and login
- **Cart Management** — Full CRUD operations for cart items
- **Order Processing** — Create, view, and manage orders
- **Admin Routes** — Protected admin endpoints for management
- **MongoDB Database** — Persistent data storage with Mongoose ODM
- **Error Handling** — Global error handler with meaningful responses

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| HTML5 | Structure & Semantic Markup |
| CSS3 | Styling, Animations & Responsive Design |
| JavaScript (ES6+) | Logic, DOM Manipulation & API Integration |
| Font Awesome | Icons |
| Google Fonts | Typography (Inter, Playfair Display) |

### Backend
| Technology | Purpose |
|---|---|
| Node.js | Runtime Environment |
| Express.js | Web Framework |
| MongoDB | NoSQL Database |
| Mongoose | ODM for MongoDB |
| JWT | Authentication Tokens |
| bcrypt.js | Password Hashing |
| CORS | Cross-Origin Resource Sharing |
| dotenv | Environment Variables |

---

## 📁 Project Structure

```
RN-nursary-project/
├── README.md
├── .gitignore
│
├── rnproject/                  # Frontend
│   ├── index.html              # Home page (main landing)
│   ├── about.html              # About page
│   ├── service.html            # Services page
│   ├── plants.html             # Plant store / catalog
│   ├── contact.html            # Contact page
│   ├── blog.html               # Blog page
│   ├── login.html              # Login / Register page
│   ├── cart.html               # Shopping cart
│   ├── checkout.html           # Checkout page
│   ├── orders.html             # Order history
│   ├── order-success.html      # Order confirmation
│   ├── admin.html              # Admin dashboard
│   ├── home.html               # Alternate home page
│   ├── style.css               # Global stylesheet
│   ├── app.js                  # Main frontend logic
│   ├── api.js                  # API service layer
│   ├── admin.js                # Admin dashboard logic
│   └── assets/                 # Images & media
│
└── Backend/                    # Backend API
    ├── server.js               # Express app entry point
    ├── package.json            # Dependencies & scripts
    ├── .env                    # Environment variables
    ├── .gitignore              # Git ignore for backend
    ├── seedAdmin.js            # Admin seeder script
    ├── config/
    │   └── db.js               # MongoDB connection config
    ├── middleware/
    │   └── auth.js             # JWT auth middleware
    ├── models/
    │   ├── User.js             # User model (Mongoose)
    │   ├── Cart.js             # Cart model (Mongoose)
    │   └── Order.js            # Order model (Mongoose)
    └── routes/
        ├── auth.routes.js      # Auth routes (register/login)
        ├── user.routes.js      # User profile routes
        ├── cart.routes.js      # Cart CRUD routes
        ├── orders.routes.js    # Order management routes
        └── admin.routes.js     # Admin management routes
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **MongoDB** (local instance or MongoDB Atlas)
- **Git**

### 1. Clone the Repository

```bash
git clone https://github.com/manishdabade45/RN-nursary-project.git
cd RN-nursary-project
```

### 2. Setup Backend

```bash
cd Backend
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the `Backend/` directory:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/rn-agritech
JWT_SECRET=your_jwt_secret_key
```

### 4. Start the Backend Server

```bash
# Development mode (with auto-reload)
npm run dev

# Production mode
npm start
```

The API will be running at `http://localhost:5000`

### 5. Seed Admin User (Optional)

```bash
node seedAdmin.js
```

### 6. Open the Frontend

Open `rnproject/index.html` in your browser, or use a local server:

```bash
# Using VS Code Live Server, or:
npx serve rnproject
```

---

## 📡 API Endpoints

### Health Check
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/health` | API health status |

### Authentication
| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/auth/register` | Register a new user |
| `POST` | `/api/auth/login` | Login & get JWT token |

### User
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/users/profile` | Get user profile |
| `PUT` | `/api/users/profile` | Update user profile |

### Cart
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/cart` | Get user's cart |
| `POST` | `/api/cart` | Add item to cart |
| `PUT` | `/api/cart/:id` | Update cart item quantity |
| `DELETE` | `/api/cart/:id` | Remove item from cart |

### Orders
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/orders` | Get user's orders |
| `POST` | `/api/orders` | Place a new order |

### Admin
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/admin/users` | Get all users |
| `GET` | `/api/admin/orders` | Get all orders |
| `PATCH` | `/api/admin/orders/:id` | Update order status |

> 🔒 All routes except `/api/auth/*` and `/api/health` require a valid JWT token in the `Authorization` header.

---

## 🌐 Deployment

### Frontend
The frontend is deployed on **Vercel** as a static site:
- URL: [https://rn-nursary-project.vercel.app](https://rn-nursary-project.vercel.app/index.html)

### Backend
The backend can be deployed on platforms like:
- **Render**
- **Railway**
- **Vercel (Serverless Functions)**
- **Heroku**

Make sure to set the environment variables (`MONGODB_URI`, `JWT_SECRET`) on the hosting platform.

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

---

## 📜 License

This project is licensed under the **ISC License**.

---

## 📞 Contact

**R.N. Agritech Services**

- 📍 A-2/12, Maniratna Angan, Manjri Road, Hadapsar, Pune - 411028
- 📞 +91 9422009218 | +91 8087835888
- 📧 shinden53@yahoo.in
- 🌐 [Website](https://rn-nursary-project.vercel.app/index.html)
- 💻 [GitHub](https://github.com/manishdabade45/RN-nursary-project)

---

<p align="center">Made with 💚 by R.N. Agritech Services Team</p>
