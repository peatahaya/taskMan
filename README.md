Django Task Manager

A simple CRUD (Create, Read, Update, Delete) web application for task management, built in Python using the Django framework. This project showcases skills in backend development, automated testing, and basic web application security. The application was developed and tested in a Kali Linux environment, utilizing end-to-end tests with Playwright and penetration testing with OWASP ZAP, sqlmap, and Nikto.

Features

Task Management: Create, view, edit, and delete tasks with fields for title, description, and completion status.

Responsive Interface: Uses Bootstrap 4 for an aesthetic and functional frontend.

Automated Testing: End-to-end tests with Playwright covering CRUD operations.

Security: Protections against CSRF, XSS, and basic security headers.

Technologies

Backend: Python 3.11, Django 5.0, SQLite



Frontend: Django templates, Bootstrap 4



Automated Testing: Playwright 1.47.0, Pytest 8.3.2



Penetration Testing: OWASP ZAP, sqlmap, Nikto



Environment: Kali Linux



Tools: Visual Studio Code, Git

Installation on Kali Linux

Prerequisites

Python 3.11+
Node.js (for Playwright)
Git
Chromium (for Playwright tests)

Installation Steps

Clone the repository:

git clone https://github.com/YourUsername/django-task-manager.git
cd django-task-manager

Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate

Install system dependencies:

sudo apt update
sudo apt install -y python3-dev libpq-dev chromium-browser

Install Python dependencies:

pip install -r requirements.txt

Apply database migrations:

python3 manage.py makemigrations
python3 manage.py migrate

Collect static files:

python3 manage.py collectstatic

Run the server:

python3 manage.py runserver

Open the application in a browser at http://127.0.0.1:8000/.

Optional: Create a Superuser

To access the Django admin panel:

python3 manage.py createsuperuser

Log in at http://127.0.0.1:8000/admin/.

Automated Testing

Install Playwright browsers:

playwright install

Run the Django server in a separate terminal:

python3 manage.py runserver



Run the tests:

pytest tests/test_playwright.py --headed

The tests verify CRUD functionality, including task creation, editing, and deletion.

Penetration Testing

The following security tests were conducted:

Manual: Tested for SQL Injection, XSS, and CSRF vulnerabilities.
Automated: Used OWASP ZAP, sqlmap, and Nikto for application scanning.



Results: The application is secured against basic attacks (CSRF, XSS) through CSRF tokens, data escaping, and security headers (e.g., X-Content-Type-Options, X-XSS-Protection).

A detailed penetration testing report is available in the security_report.md file.
