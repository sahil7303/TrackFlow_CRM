
# TrackFlow- CRM Application

TrackFlow-CRM is a web-based Customer Relationship Management (CRM) platform built with Django, Python, and MySQL. This application provides an efficient way to manage customer-related data with user authentication and full CRUD operations support.

## Features

- **User Authentication** - Secure registration, login, and logout functionality to protect user data and maintain privacy
- **Record Management** - Complete CRUD operations for customer records, allowing seamless data management
- **MySQL Integration** - Robust database backend for reliable data storage and retrieval


## Tech Stack

- Python
- Django 
- MySQL

## Project Structure
```bash
dcrm/
├── dcrm/
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── website/
│   ├── migrations/
│   ├── templates/
│   │   ├── add_record.html
│   │   ├── base.html
│   │   ├── home.html
│   │   ├── navbar.html
│   │   ├── record.html
│   │   ├── register.html
│   │   └── update_record.html
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
└── manage.py
```
## Installation


 1. Clone the repository

```bash
git clone <repository-url>
cd <directory>
```
    

 2. Create and activate virtual environment

```bash
# Create virtual environment
python -m venv crm_env

# Activate virtual environment
# For Linux/macOS:
source crm_env/bin/activate

# For Windows:
crm_env\Scripts\activate
```
3. Install Dependencies

```bash
pip install -r requirements.txt
```

4. Configure database settings in `settings.py`

```bash
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'crmdb',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

5. Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

6. Start Development server
```bash
python manage.py runserver
```

7. Visit `http://127.0.0.1:8000/` in your browser.



## Key Components

- `settings.py` - Project configuration and database settings
- `urls.py` - URL routing management
- `models.py` - Database structure definitions
- `views.py` - Request handling logic and template rendering
- `templates/` - Frontend HTML templates

## Templates

- `base.html` - Primary template with common elements
- `home.html` - Dashboard for logged-in users
- `add_record.html` - New customer record form
- `update_record.html` - Existing record update form
- `register.html` - User registration interface
- `record.html` - Individual customer record view
- `navbar.html` - Navigation component