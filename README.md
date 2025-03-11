# React + Django Blog App

A full-stack blog application built using **React (frontend)** and **Django REST Framework (backend)**.

## 🚀 Features
- View all blog posts
- View a single post's details
- Create a new blog post
- REST API with Django backend
- React frontend with API integration

---

## 🛠️ Technologies Used
### **Backend (Django REST Framework)**
- Django
- Django REST Framework
- Gunicorn (for production)
- CORS Headers (for frontend communication)

### **Frontend (React.js)**
- React.js
- React Router
- Axios (for API calls)
- TailwindCSS (optional for styling)

---

## 📌 Setup Instructions

### **1️⃣ Backend (Django API Setup)**
#### **Step 1: Clone the repository & Install dependencies**
```sh
# Clone the repository
git clone https://github.com/yourusername/django-react-fullstack.git
cd django-react-fullstack

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # (Windows: venv\Scripts\activate)

# Install dependencies
pip install -r requirements.txt
```

#### **Step 2: Configure Database & Migrate**
```sh
python manage.py migrate
```

#### **Step 3: Run the Development Server**
```sh
python manage.py runserver
```
The API will be available at: **http://127.0.0.1:8000/api/posts/**

---

### **2️⃣ Frontend (React Setup)**
#### **Step 1: Install dependencies**
```sh
cd ../frontend  # Move to the frontend folder
npm install
```

#### **Step 2: Configure API URL**
Modify `src/api.js` to match your backend URL:
```javascript
const API_URL = "http://127.0.0.1:8000/api/posts/"; // Change if using production
```

#### **Step 3: Run React Development Server**
```sh
npm start
```
The React app will be available at: **http://localhost:3000/**

---

## 🚀 Deployment

### **1️⃣ Deploy Django Backend**
- **Recommended Hosting:** Render, Railway, DigitalOcean, Heroku, etc.
- **Example using Render:**
  1. Push Django project to GitHub
  2. Go to [Render](https://render.com) and create a new Web Service
  3. Connect to your GitHub repo
  4. Set build command: `gunicorn myproject.wsgi --log-file -`
  5. Deploy!

### **2️⃣ Deploy React Frontend**
- **Recommended Hosting:** Vercel, Netlify, Firebase, etc.
- **Example using Vercel:**
  ```sh
  npm install -g vercel
  vercel login
  vercel
  ```

---

## 🎉 Usage
- **Visit `/`** → View all blog posts
- **Click on a post** → See post details
- **Visit `/create`** → Create a new post

---

## 📄 API Endpoints
| Method | Endpoint        | Description          |
|--------|----------------|----------------------|
| GET    | `/api/posts/`  | Fetch all posts     |
| GET    | `/api/posts/:id/` | Fetch a single post |
| POST   | `/api/posts/`  | Create a new post   |

---

## 🛠️ Future Improvements
- User authentication (login/logout)
- Edit/Delete blog posts
- Image uploads for posts

---

## 📌 Contributing
Feel free to submit a pull request or report issues.

---

## 💡 Author
Created by **Your Name** 🚀

---

## 📜 License
This project is open-source under the **MIT License**.

