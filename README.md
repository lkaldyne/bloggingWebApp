# Fully featured webapp made in django.
This web-app is currently set up for blogging and posting content, but can act as a template for any web app involving secure user account management.

Features include:
- User registration
- User login/logout
- User sessions with cookies for maintained login status
- Profile section
  - Account properties with modification options (email, username, etc.)
  - Profile picture upload from user's local system
- Post creation
- Post modification
- Post deletion
- View other user's posts, but only content owners can delete/edit their posts
- Request for password reset, app will send an email with encrypted one-time link to reset the password

Security features such as form CSRF tokens and SHA-256 encrypted DB information have been implemented in this project.

# Setup instructions
To get this solution running on your system:
1. Install python 3.x
2. Use pip (or other package installer of your choice) to install Django, Pillow, and smtplib
3. In the main directory of the project, run the command "python manage.py runserver". This will run the project on a localhost port and provide a link to navigate directly to your locally hosted app

Note. In order for password reset functionality to work, environment variables "EMAIL_USER" and "EMAIL_PASS" must be created on the system the app is running on. The variables should contain the email and password, respectively, of the email address you wish for django to use to send password reset links to clients. 
