# **MERN Todo App (Frontend)**

This is the **frontend** of the **MERN Todo Application**, built using **React.js**.
It allows users to **sign up, log in, manage todos (create, read, update, delete)**, and securely **log out** using **JWT authentication**.

---

## **Live Demo**

**Frontend URL:** [https://front-end-psi-gules.vercel.app/](https://front-end-psi-gules.vercel.app/)
**Backend API Base URL:** (configured in `.env` file as `VITE_API_BASE_URL`)

---

## **Features**

- User Authentication (Signup & Login)

- JWT Token-based Authorization
- Create, Read, Update, and Delete (CRUD) Todos
- Edit todo text and toggle completion status
- Logout functionality
- Toast Notifications for feedback
- Protected routes using React Router
- Modern UI with TailwindCSS

---

## **Tech Stack**

**Frontend:**

- React.js
- React Router DOM
- Axios
- React Hot Toast
- Tailwind CSS
- Vite

**Backend:**

- Node.js
- Express.js
- MongoDB
- JWT Authentication

---

## **Setup Instructions**

### 1. Clone the Repository

```bash
https://github.com/ShradhaSuman7-eng/FrontEnd.git
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory and add:

```env
VITE_API_BASE_URL=https://your-backend-url.onrender.com/api
```

### 4 .Start the Development Server

```bash
npm run dev
```

Then open [http://localhost:5173](http://localhost:5173) in your browser.

---

## **Project Structure**

```
frontend/
├── public/
├── src/
│   ├── components/
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Signup.jsx
│   │   ├── PageNotfound.jsx
│   ├── App.jsx
│   ├── App.css
│   ├── main.jsx
│
├── .env
├── package.json
├── vite.config.js
└── README.md
```

---

## **Authentication Flow**

- **Signup** → Creates new user → redirects to Login
- **Login** → Validates user and stores `jwt` in `localStorage`
- **Protected Home Route** → Accessible only if JWT exists
- **Logout** → Clears `jwt` and redirects to `/login`

---

## **Key Components**

### `Home.jsx`

- Displays todos
- Allows creating, editing, deleting, and toggling completion
- Handles logout

### `Login.jsx`

- Authenticates user
- Stores JWT in `localStorage`
- Redirects to `/` on success

### `Signup.jsx`

- Registers a new user
- Redirects to login

### `PageNotfound.jsx`

- Handles invalid routes

---

## **API Endpoints (Backend)**

| Method   | Endpoint           | Description               |
| -------- | ------------------ | ------------------------- |
| `POST`   | `/user/signup`     | Register a new user       |
| `POST`   | `/user/login`      | Login and get JWT token   |
| `GET`    | `/user/logout`     | Logout user               |
| `GET`    | `/todo/fetch`      | Fetch all todos           |
| `POST`   | `/todo/create`     | Create a new todo         |
| `PUT`    | `/todo/update/:id` | Update todo (status/text) |
| `DELETE` | `/todo/delete/:id` | Delete todo               |

#### GitHub: https://github.com/ShradhaSuman7-eng/FrontEnd.git
