# Soundwave 🎧
### Full-Stack Audio E-Commerce Platform

Soundwave is a full-stack e-commerce web application for browsing and managing audio products. It features a customer-facing shopping experience alongside a dedicated administration panel for managing customers and product brands.

The application focuses on secure authentication, account management, address management, image uploads, and administrative control, built using Node.js, Express.js and MongoDB.

---

## ✨ Features

### 👤 Customer Features

- **User Authentication:** Registration and login with password hashing using bcrypt.
- **Email OTP Verification:** Email-based OTP verification during authentication.
- **Google Authentication:** Google OAuth 2.0 integration using Passport.js.
- **Password Recovery:** Forgot-password and reset-password workflows with OTP verification.
- **User Profile Management:** View and update personal information.
- **Address Management:** Add, edit, view and delete delivery addresses.
- **Profile Image Upload:** Upload and manage profile pictures.
- **Session Management:** Authentication sessions with protected routes.

### 🛠️ Admin Features

- **Admin Dashboard:** Centralised administration interface.
- **Customer Management:** View, search and manage registered customers.
- **Block / Unblock Customers:** Control customer account access.
- **Customer Details:** View individual customer information and associated records.
- **Brand Management:** Create, edit, view and delete product brands.
- **Brand Status Management:** Activate or deactivate brands.
- **Image Uploads:** Upload brand logos using Cloudinary.

### 🎨 User Interface

- Server-rendered pages using EJS.
- Responsive layouts with Tailwind CSS.
- Custom notifications and confirmation modals.
- Separate customer and administrator interfaces.

---

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Runtime | Node.js |
| Backend | Express.js |
| Database | MongoDB |
| ODM | Mongoose |
| Templating | EJS |
| Styling | Tailwind CSS |
| Frontend Interactions | Vanilla JavaScript |
| Authentication | Passport.js, Google OAuth 2.0 |
| Password Security | bcryptjs |
| Session Management | express-session |
| Image Storage | Cloudinary |
| File Uploads | Multer |
| Email Services | Nodemailer |
| Validation | express-validator |

---

## 🏗️ Project Architecture

The application follows an MVC-inspired structure with separate responsibilities for routes, controllers, middleware, services, models and views.

```text
Soundwave/
│
├── public/
│   └── images/
│
├── src/
│   ├── config/
│   │   ├── db.js
│   │   ├── cloudinary.js
│   │   └── passport.js
│   │
│   ├── controllers/
│   │
│   ├── middleware/
│   │
│   ├── models/
│   │
│   ├── routes/
│   │
│   ├── scripts/
│   │
│   ├── services/
│   │
│   ├── views/
│   │   ├── admin/
│   │   ├── auth/
│   │   ├── partials/
│   │   └── user/
│   │
│   ├── app.js
│   └── server.js
│
├── package.json
├── package-lock.json
└── README.md
```

---

## 🔐 Authentication Flow

Soundwave implements an email OTP verification flow alongside traditional and Google authentication.

**Email and Password Authentication**

1. User registration with name, email and password.
2. Password hashing using bcrypt.
3. Email verification through OTP.
4. OTP validation before granting authenticated access.
5. Session-based access to protected customer pages.

**Google Authentication**

- Google OAuth 2.0 integration through Passport.js.
- User authentication using Google accounts.

**Password Recovery**

- Request password reset.
- Receive and verify an email OTP.
- Reset the account password.

---

## ⚙️ Installation and Setup

### Prerequisites

- Node.js
- npm
- MongoDB
- Cloudinary account
- SMTP email credentials
- Google OAuth credentials (for Google authentication)

### 1. Clone the Repository

```bash
git clone https://github.com/ashwinmuralinair2002/Soundwave.git
```

### 2. Navigate to the Project

```bash
cd Soundwave
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env` file in the project root.

Add the required configuration:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_session_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

SMTP_HOST=your_smtp_host
SMTP_PORT=587
SMTP_USER=your_smtp_username
SMTP_PASS=your_smtp_password
EMAIL_FROM=your_sender_email

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=your_google_callback_url
```

Use your own credentials and keep the `.env` file private. Configure the values required by the features you intend to use.

### 5. Start the Application

For development:

```bash
npm run dev
```

For production:

```bash
npm start
```

The server uses port `5000` by default, unless another port is configured through the environment.

---

## 🗺️ Development Scope

The project has been developed in stages, with a focus on building the customer authentication and administration foundation before expanding the shopping functionality.

Current implemented areas include:

- Customer authentication and OTP verification
- Google authentication integration
- Profile and address management
- Admin dashboard
- Customer administration
- Brand management

Further development areas include deeper product catalogue functionality, order processing, coupon management and payment gateway integration.

---

## 👨‍💻 Author

**Ashwin Murali Nair**

- GitHub: [@ashwinmuralinair2002](https://github.com/ashwinmuralinair2002)
- Project: [Soundwave](https://github.com/ashwinmuralinair2002/Soundwave)

---

*Soundwave is an independent educational full-stack development project.*
