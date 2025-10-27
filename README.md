# Flask Admin Dashboard

A modern, secure, and Docker-ready **Flask Admin Dashboard** with **MySQL backend** 

---

## 🔹 Features

### Admin Dashboard
- Login / Logout system 
- Register new admins
- View total admins, messages, and activity counts
- Modern responsive UI with Bootstrap 5
- Dashboard cards with gradient and shadow effects

### API Endpoints
-/register** – Register a new admin  
-/login** – Login admin and get admin ID   

### Database
- MySQL backend (`admindb`)
- Tables:
  - `admin`: Stores admin credentials (hashed passwords)  
- Auto table creation on app startup

---

## 🔹 Requirements

- Python 3.10+  
- Flask 2.3+  
- MySQL 8+  
- Docker (optional for containerization)  

Python packages:

```bash
pip install Flask Flask-MySQLdb flask-cors
```
🔹 Environment Variables

Set the following variables for MySQL:
```MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=yourpassword
MYSQL_DB=admindb
```
🔹 Running Locally

1. Clone the repo:
```
git clone https://github.com/Mr-Rko/flask-admin-dashboard.git
cd flask-admin-dashboard
```
2. Set environment variables (or use .env file):
```
export MYSQL_HOST=localhost
export MYSQL_USER=root
export MYSQL_PASSWORD=yourpassword
export MYSQL_DB=admindb
```
3. Run the app:
```
python app.py

```
4. Open in browser: http://localhost:5000

## 🔹 Docker Setup (Optional)

1. Build Docker image:
```
docker build -t Dockerfile .
```
2. Run Docker container:
```
docker run -d -p 5000:5000 --name flask-admin-app \
-e MYSQL_HOST=<mysql_host> \
-e MYSQL_USER=<mysql_user> \
-e MYSQL_PASSWORD=<mysql_password> \
-e MYSQL_DB=<mysql_db> \
flask-admin-app
```


