# 📚 Library Management System as Keywordio Intern Task

Hii my name is Harsh A Dubey, got an **Django Internship** task so the is the documentation. 
A Library Management System built using **Django** and **Django REST Framework (DRF)** that allows admins to manage books through CRUD operations and provides a student view to browse available books.

## 🛠️ Features

### Admin Operations
- **Signup**: Register a new admin account (ensuring unique email addresses).
- **Login**: Authenticate using username and password.
- **CRUD on Books**:
  - **Create**: Add a new book.
  - **Read**: Retrieve all book records.
  - **Update**: Modify existing book details.
  - **Delete**: Remove a book from the system.

### Student View
- **List Books**: View all available books.

## 🏗️ Tech Stack
- **Backend**: Django (v4.x) & Django REST Framework (v3.x)
- **Database**: MySQL
- **Authentication**: Token-based authentication (using DRF's `TokenAuthentication`)

## 📂 Project Structure
```
├── keywordio-inter-task/
    ├── library-management/
        ├── librarymanagement/
        │   ├── __init__.py
        │   ├── settings.py
        │   ├── urls.py
        │   ├── asgi.py
        │   └── wsgi.py
        ├── library/
        │   ├── __init__.py
        │   ├── models.py
        │   ├── views.py
        │   ├── urls.py
        │   ├── tests.py
        │   ├── apps.py
        │   ├── migrations/
        │   │   ├── __init__.py
        │   │   ├── ...
        │   └── admin.py
        ├── db.sqlite3
        ├── requirements.txt
        ├──Static/
        │   ├── images/
        ├── templates/
        ├──library/
        │   ├── index.html
        │   ├── ...
        └── manage.py
        └── README.md
        └── .gitignore
```

## 🚀 Getting Started

### Prerequisites
Ensure you have the following installed:
- Python 3.10+
- MySQL
- Virtual Environment (recommended)

### Setup Instructions

1. **Clone the repository:**
```bash
git clone https://github.com/harshuCodes-git/Keywordio-inter-task.git
cd library-management
```

2. **Create and activate a virtual environment:**
```bash
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
```

3. **Install dependencies:**
```bash
pip install -r requirements.txt
```



4. **Run migrations:**
```bash
python manage.py makemigrations
python manage.py migrate
```

5. **Start the development server:**
```bash
python manage.py runserver
```

## 📊 API Endpoints

### Admin Authentication

1. **Signup**: `POST /api/admin/signup/`
```json
{
  "email": "admin@example.com",
  "password": "yourpassword"
}
```

2. **Login to check**: `POST /api/admin/login/`
```json
{
  "username": "admin",
  "password": "admin"
}
```
Response:
```json
{
  "token": "your_auth_token"
}
```

### Book Management (Authenticated Admin Only)

1. **Create Book**: `POST /api/books/`
```json
{
  "title": "Django for Beginners",
  "author": "William S. Vincent",
  "isbn": "978-1983172666",
  "published_date": "2022-05-15"
}
```

2. **Get All Books**: `GET /api/books/`

3. **Update Book**: `PUT /api/books/{id}/`

4. **Delete Book**: `DELETE /api/books/{id}/`

### Student View

- **List Books**: `GET /api/books/`

## 🧪 Testing
Run tests to ensure functionality:
```bash
python manage.py test
```


4. Feedback: Continuous improvement based on user feedback and AI learning.


    


