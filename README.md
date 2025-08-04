# Roots – MERN E-Commerce Platform

> **Frontend:** React JS  
> **Backend:** Node JS & Express JS  
> **Database:** MongoDB (Atlas)

---

## 📦 Installation Guide

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/roots.git
cd roots
```

### 2. Install Dependencies

#### Backend Dependencies
```bash
cd roots
npm install
```

#### Frontend Dependencies
```bash
cd client
npm install
```

---

## ⚙️ Environment Configuration

### 1. Backend `.env` Setup
Create a `.env` file inside the `roots/` directory with the following content:

```env
MONGODB_URI=mongodb+srv://nigga:nigga@root1234.65vo9un.mongodb.net/
JWT_SECRET=your_jwt_secret
BRAINTREE_MERCHANT_ID=your_braintree_merchant_id
BRAINTREE_PUBLIC_KEY=your_braintree_public_key
BRAINTREE_PRIVATE_KEY=your_braintree_private_key
```

> Replace the sample credentials with your actual secure values.

---

### 2. Frontend `.env` Setup
Inside the `client/` folder, create a `.env` file:

```env
REACT_APP_API_URL=http://localhost:5000/api
```

> Use the correct base URL depending on whether you are running locally or deploying.

---

## 🚀 Running the App Locally

In the root project folder (`roots`):

```bash
npm run dev
```

> This command will start both the backend and frontend servers concurrently using `concurrently`.

---

## 🧩 Database Structure

| Collection  | Fields |
|-------------|--------|
| `categories` | `_id`, `name`, `createdAt`, `updatedAt` |
| `orders`     | `_id`, `status`, `products[]`, `transaction_id`, `amount`, `address`, `user`, `createdAt`, `updatedAt` |
| `products`   | `_id`, `photo`, `sold`, `name`, `description`, `price`, `category`, `shipping`, `quantity`, `createdAt`, `updatedAt` |
| `users`      | `_id`, `role`, `history[]`, `name`, `email`, `salt`, `hashed_password`, `createdAt`, `updatedAt` |

---

## 📝 App Features

### User Features:
- View all products
- View individual product details
- Filter products by category and price
- Add to cart and checkout with credit card
- Register and login

### Admin Features:
- Create, edit, update, and delete products
- Manage product categories
- View ordered products
- Change order status (e.g., Processing, Shipped, Delivered)

---

## 👨‍💼 Admin Credentials (For Testing)

> To assign admin privileges to any user, change the `role` field from `0` to `1` in MongoDB using Compass or CLI.

---

## 🔒 Notes

- Do not commit `.env` files to GitHub. Add `.env` to your `.gitignore`.
- Always secure your credentials and secrets.
- Use environment variables for production deployment instead of hardcoding.

---