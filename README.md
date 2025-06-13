# School LMS

School LMS is a comprehensive web application designed for educational institutions to manage online learning platforms, including course management, student enrollment, and payment processing.

## Features

- User authentication and authorization
- Course management
- Student enrollment system
- Payment processing
- Admin dashboard
- Responsive design

## Technologies Used

*   **Backend**: Python, Django, Django REST Framework
*   **Database**: PostgreSQL (recommended), SQLite3
*   **Other**: pip, Git

## Security Considerations

It is crucial to follow security best practices during development and deployment:
*   Always keep your `SECRET_KEY` confidential and use environment variables for sensitive data.
*   Ensure `DEBUG` is set to `False` in production.
*   Regularly update dependencies to patch known vulnerabilities.
*   Implement proper input validation and sanitization to prevent common web vulnerabilities (e.g., SQL injection, XSS).
*   Use HTTPS in production to encrypt communication.

## Prerequisites

- Python 3.12+
- PostgreSQL 13+ (recommended) or SQLite3
- pip (Python package manager)
- Git

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Saman-naruee/schoollms.git
cd schoollms
```

### 2. Create and Activate Virtual Environment

```bash
# Windows
python -m venv env
.\env\Scripts\activate

# Linux/MacOS
python3 -m venv env
source env/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## Database Setup

### Option 1: PostgreSQL (Recommended for Production)

1. Install PostgreSQL if you haven't already
2. Create a new database and user
3. Create a `.env` file in the project root with the following variables:

```env
DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_HOST=localhost
DB_PORT=5432
```

### Option 2: SQLite (Development)

For development, you can use SQLite by modifying the database settings in `schoollms/settings.py`:

```python
DATABASES = SQLITE_DB  # Change from POSTGRES_DB to SQLITE_DB
```

## Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

## Create Superuser

```bash
python manage.py createsuperuser
```

## Running the Development Server

```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` in your browser to access the application. The Django Admin panel will be available at `http://127.0.0.1:8000/admin/` after creating a superuser.

## Environment Variables

Create a `.env` file in the project root with the following variables:

```env
DEBUG=True
SECRET_KEY=your-secret-key-here
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=5432
```

## Project Structure

```
schoollms/
├── manage.py           # Django management script
├── requirements.txt    # Project dependencies
├── .env               # Environment variables
├── .gitignore
└── schoollms/         # Main project configuration
    ├── __init__.py
    ├── settings.py     # Django settings
    ├── urls.py        # Main URL configuration
    └── wsgi.py        # WSGI configuration
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, email samannaruee@gmail.com or open an issue in the repository.
