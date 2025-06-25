Here's the updated README.md tailored to your exact project structure:

```markdown
# 🚀 InventX – Inventory Management System (MERN Stack)

**InventX** is a full-stack inventory management web application that helps users track products, monitor stock, and manage warehouses in real-time. It supports role-based access, secure authentication, and cloud image uploads — designed with scalability, validation, and modular architecture in mind.

---

## 🌐 Tech Stack

### 🧠 Backend
- **Node.js**, **Express.js**
- **MongoDB** with Mongoose
- **JWT Auth**, **Bcrypt**, **Cookie-based Sessions**
- **Cloudinary** for image hosting
- **Zod** for schema validation
- **Nodemailer** for contact/reset email flows

### 🎨 Frontend
- **React.js** with Hooks
- **Redux Toolkit** for state management
- **React Router** for routing
- **React Quill** for rich product descriptions
- **React Toastify** for notifications
- **SCSS Modules** for scoped styling
- **Zod** client-side validation

---

## 📦 Features

### ✅ Authentication
- Secure Register/Login/Logout
- JWT + HttpOnly cookie-based auth
- Password hashing (bcrypt)
- Forgot/reset password (with email token)
- Protected routes with `HiddenLink` component

### 📦 Product Management
- Add/edit/delete/view products
- Product image upload via Cloudinary
- Rich text descriptions (React Quill)
- SKU auto-generation (timestamp-based)
- View product details with created/updated timestamps
- Product filtering and search

### 📊 Dashboard Analytics
- Total inventory value calculation
- Out-of-stock product alerts
- Category distribution tracking
- Responsive product summary cards

### 📥 Contact Form
- Send messages to admin (Nodemailer-powered)

---

## 📁 Project Structure (Actual Implementation)

```
bhargavzz-inventx/
├── README.md
├── .gitattributes
├── backend/
│   ├── package.json
│   ├── server.js
│   ├── .gitignore
│   ├── controllers/
│   │   ├── contactController.js
│   │   ├── productController.js
│   │   └── userController.js
│   ├── middleWare/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── models/
│   │   ├── productModel.js
│   │   └── userModel.js
│   ├── routes/
│   │   ├── contactRoute.js
│   │   ├── productRoute.js
│   │   └── userRoute.js
│   ├── uploads/
│   │   └── .gitkeep
│   └── utils/
│       ├── fileUpload.js    # Cloudinary integration
│       └── sendEmail.js     # Nodemailer configuration
└── frontend/
    ├── package.json
    ├── .gitignore
    ├── public/
    │   ├── index.html
    │   └── manifest.json
    └── src/
        ├── App.js
        ├── index.js
        ├── components/
        │   ├── card/                # Reusable card component
        │   ├── changePassword/      # Password update UI
        │   ├── footer/              # App footer
        │   ├── header/              # Navigation header
        │   ├── infoBox/             # Dashboard metrics
        │   ├── layout/              # Main layout wrapper
        │   ├── loader/              # Loading indicators
        │   ├── product/             # All product components
        │   │   ├── productDetail/   # Single product view
        │   │   ├── productForm/     # Add/edit form
        │   │   ├── productList/     # Product listing table
        │   │   └── productSummary/   # Inventory summary cards
        │   ├── protect/             # Auth protection (HiddenLink)
        │   ├── search/              # Search functionality
        │   └── sidebar/             # Navigation sidebar
        ├── customHook/
        │   └── useRedirectLoggedOutUser.js  # Auth redirection
        ├── data/
        │   └── sidebar.js           # Navigation configuration
        ├── pages/                   # Application views
        │   ├── addProduct/         # Add new product
        │   ├── auth/                # Login/Register
        │   ├── contact/             # Contact admin
        │   ├── dashboard/           # Main dashboard
        │   ├── editProduct/         # Edit existing product
        │   ├── Home/                # Landing page
        │   └── profile/             # User profile management
        ├── redux/                   # State management
        │   ├── store.js             # Redux store
        │   └── features/
        │       ├── auth/            # Authentication slice
        │       └── product/         # Product state + filters
        ├── schemas/                 # Validation schemas
        │   ├── authSchema.js
        │   └── productSchema.js
        └── services/                # API services
            └── authService.js
```

---

## 🔐 Environment Variables

### Backend `.env` (create in `/backend`)
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email_address
EMAIL_PASS=your_email_password
EMAIL_HOST=smtp_provider_host
FRONTEND_URL=http://localhost:3000
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### Frontend `.env` (create in `/frontend`)
```env
REACT_APP_BACKEND_URL=http://localhost:5000
```

---

## 🛠️ Getting Started

### 1. Clone Repository
```bash
git clone https://github.com/Bhargavzz/inventx.git
cd bhargavzz-inventx
```

### 2. Install Dependencies
```bash
# Backend setup
cd backend
npm install

# Frontend setup
cd ../frontend
npm install
```

### 3. Start Development Servers
```bash
# Run backend (from /backend directory)
npm run dev

# Run frontend (from /frontend directory)
npm start
```
Access application at: `http://localhost:3000`

---

## ✅ Key Implementation Details

1. **Authentication Flow**:
   - JWT stored in HttpOnly cookies for security
   - Password reset via Nodemailer tokens
   - `useRedirectLoggedOutUser` custom hook for route protection

2. **Product Management**:
   - SKU generation using timestamps
   - Rich text descriptions with React Quill
   - Image uploads handled through Cloudinary middleware
   - Redux-powered state management for product data

3. **State Management**:
   - Redux Toolkit slices for auth and products
   - Filter slice for product search/sorting
   - Async thunks for API communication

4. **Validation**:
   - Zod schemas for both frontend and backend
   - Consistent validation rules across client/server

---

## ✅ Future Improvements
- Role-based access control (Admin/User)
- Bulk CSV product import/export
- Unit/Integration testing (Jest)
- Docker containerization
- PDF stock report generation
- ElasticSearch integration

---

## 👨‍💻 Author
**Sitra Vishnu Bhargav**  
Final-year CSE, IIIT Jabalpur  
[GitHub](https://github.com/Bhargavzz) • [LinkedIn](https://linkedin.com/in/bhargavzz)

---

## 🛡️ License
This project is licensed under the [MIT License](LICENSE).
```

