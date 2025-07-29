# Django Login System with Google Authentication

A complete user authentication system built with **Django**, **HTML**, **CSS**, and **Bootstrap**.  
It supports:

- ✅ User registration (sign up)
- ✅ User login/logout
- ✅ Google OAuth2 Sign-In (via `python-social-auth`)

---

## 🔧 Tech Stack

- **Backend**: Django (Python)
- **Frontend**: HTML, CSS, Bootstrap 5
- **OAuth2**: Google Sign-In using `social-auth-app-django`

---

## ✨ Features

- Simple & responsive login page
- Django user authentication
- Secure sign-up and login
- Google account sign-in integration
- Form validation and error handling

---

## 🚀 Getting Started

To run locally, do the usual:
1. Clone the repository:
   ```
   git clone https://github.com/hardeep04/LoginSystem.git
   ```
2. Move inside the folder
   ```
   cd LoginSystem
   ```
3. Install the requirements:
   ```
   python -m pip install -r requirements.txt
   ```
4. Google OAuth Setup:
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project → Enable OAuth Consent Screen
   - Add credentials for OAuth2 and set:
     ```
     Authorized redirect URI: http://localhost:8000/auth/complete/google-oauth2/
     ```
   - In settings.py, add:
     <pre>
     AUTHENTICATION_BACKENDS = (
     'social_core.backends.google.GoogleOAuth2',
     'django.contrib.auth.backends.ModelBackend',
     )

     SOCIAL_AUTH_GOOGLE_OAUTH2_KEY = 'your-client-id'
     SOCIAL_AUTH_GOOGLE_OAUTH2_SECRET = 'your-client-secret' </pre>  
  
5. Migrations & Run
     <pre>
     python manage.py makemigrations
     python manage.py migrate
     python manage.py runserver </pre>
