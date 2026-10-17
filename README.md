# Student Information System (SIS) – PHP & MySQL

A web-based Student Information System built with PHP and MySQL. It lets an administrator manage students, departments, courses, academic history, and system users from a single admin panel.

**Live demo:** http://sims.byethost31.com  
**Admin login:** http://sims.byethost31.com/admin/login.php

## Features

- Administrator login with session handling
- Dashboard with totals for departments, courses, students, and student academics
- Student management (add, edit, view, delete, update status)
- Student academic history (semester, year, school year, status)
- Department and course maintenance
- User list and account management
- System settings (system name, logo, and cover image)

## Tech Stack

| Layer | Technology |
|---|---|
| Server-side | PHP 8.x (mysqli) |
| Database | MySQL / MariaDB |
| Front end | AdminLTE, Bootstrap 4, jQuery, DataTables, Font Awesome |
| Web server | Apache (`.htaccess` enabled) |

## Project Structure

```
admin/      Admin pages and login
classes/    PHP classes (DBConnection, Login, Master, Users, SystemSettings)
dist/       AdminLTE CSS and JavaScript assets
inc/        Shared header and layout includes
libs/       Third-party libraries
plugins/    Front-end plugins (jQuery, Bootstrap, DataTables, etc.)
uploads/    Logo, cover, and avatar images
user/       Public-facing pages
initialize.php   Base URL and database settings
config.php       Application bootstrap
```

## Local Installation (XAMPP)

1. Copy the project folder into `C:\xampp\htdocs\sis`.
2. Start **Apache** and **MySQL** in the XAMPP control panel.
3. Open phpMyAdmin, create a database named `sis_db`, and import `sis_db_clean.sql`.
4. Check `initialize.php`:
   ```php
   define('base_url','http://localhost/sis/');
   define('DB_SERVER',"localhost");
   define('DB_USERNAME',"root");
   define('DB_PASSWORD',"");
   define('DB_NAME',"sis_db");
   ```
5. Open http://localhost/sis/admin/ in your browser.

## Deployment (ByetHost Free Hosting)

1. Create a MySQL database in the hosting panel (for example `b31_43198293_sis`).
2. Import `sis_db_clean.sql` through the panel's phpMyAdmin.
3. Edit `initialize.php` with the hosting values: `base_url`, MySQL host, username, password, and database name.
4. Upload all project files into the `htdocs` folder so that `index.php` sits directly inside it.
5. Make sure the `uploads` folder is writable.
6. Open the site and sign in to the admin panel.

> **Security note:** never commit real database passwords to a public repository. Keep production credentials only on the server.

## Demo Credentials (for evaluators)

| Field | Value |
|---|---|
| Login URL | http://sims.byethost31.com/admin/login.php |
| Username | `admin` |
| Password | `admin123` |

Change this password after evaluation.

## Author

Santos Jr., Mier – Capstone Project, Web Development 2
