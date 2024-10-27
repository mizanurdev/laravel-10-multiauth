# Laravel 10 Multi Authentication System

This project implements a **Multi-Authentication System** in Laravel 11, allowing for three types of users: **Admin**, and **User**. Each type of user has access to their own dashboard and cannot access the URLs of other user types. This is a simple but effective multi-auth setup for role-based access control.
## Author
- **Name:** Md. Mizanur Rahman
- **Email:** mizancse2018@gmail.com

## Features

- **Multi-Authentication** with three user roles: **Admin**, and **User**.
- Separate login and dashboard views for each role.
- Restricted access to other users' URLs (e.g., a **User** cannot access **Admin** dashboards).
- Basic authentication system using Laravel’s built-in authentication features.

## Installation

To set up the project locally, follow these steps:

### 1. Clone the repository:

```bash
git clone https://github.com/mizanurdev/laravel-10-multiauth.git
```
### 2. Navigate to the project directory:
```
cd laravel-10-multiauth
```

### 3. Install dependencies:
```
composer install
npm install
npm run dev
```

### 4. Set up environment configuration:
- Copy the .env.example file and rename it to .env:
```
cp .env.example .env
```
- Update the .env file with your database and other configuration details:
- note: MAIL_USERNAME=(your mailtrap username MAIL_PASSWORD=(your mailtrap password)
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_multiauth
DB_USERNAME=root
DB_PASSWORD=

MAIL_MAILER=smtp
MAIL_HOST=sandbox.smtp.mailtrap.io
MAIL_PORT=587
MAIL_USERNAME=cd55d7e9fcbefa
MAIL_PASSWORD=d78d6b12bca2c3
MAIL_ENCRYPTION=tls
```
### 5. Generate the application key:
```
php artisan key:generate
```
### 6. Set up the database
- Run the migrations to create the necessary tables:
```
php artisan migrate
```
- (Optional) Seed the database with some demo users:
```
php artisan db:seed
```
- (Optional) import sql file to your database:
set database name in env file first
#### 1. For user
- email: user@test.com
- password: 12345678
#### 2. For admin
- email: admin@test.com
- password: 12345678

### 7. Run the application:
```
php artisan serve
```
Now, the application should be running at http://127.0.0.1:8000.

### User Roles and Dashboards
This system supports three user roles: Admin, and User. Each role has access to its own login and dashboard.

- Admin: Can manage Users but has no access to Master areas.
- User: Regular users with access to user-specific functionality.

### URLs
- Admin Login: /login
- User Login: /login

After login, each user will be redirected to their respective dashboard.

- Admin Dashboard: /admin/dashboard
- User Dashboard: /dashboard

### Contributing

If you'd like to contribute to this project:

- Fork the repository.
- Create a new branch for your feature or bug fix.
- Make your changes and ensure everything works as expected.
- Submit a pull request for review.

### License
This project is licensed under the MIT License. You are free to use, modify, and distribute the code under the terms of this license.