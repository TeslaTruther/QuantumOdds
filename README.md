# [Datta Able Flask](https://appseed.us/product/datta-able/flask/)

Open-source **[Flask Dashboard](https://appseed.us/admin-dashboards/flask/)** generated by `AppSeed` on top of a modern design. **Datta Able** Bootstrap Lite is the most stylized Bootstrap 4 Lite Admin Template, around all other Lite/Free admin templates in the market. It comes with highly feature-rich pages and components with fully developer-centric code.

- 👉 [Datta Able Flask](https://appseed.us/product/datta-able/flask/) - `Product page`
- 👉 [Datta Able Flask](https://flask-datta-able.appseed-srv1.com/) - `LIVE demo` 

<br />

## Features

> `Have questions?` Contact **[Support](https://appseed.us/support/)** (Email & Discord) provided by **AppSeed**

| Free Version                          | [PRO Version](https://appseed.us/product/datta-able-pro/flask/)          | 🚀 Custom - $7,900         |  
| --------------------------------------| --------------------------------------| --------------------------------------|
| ✓ **Up-to-date dependencies**             | **Everything in Free**, plus:                                        | **Everything in PRO**, plus:       |
| ✓ Best Practices                          | ✅ **Premium Bootstrap 5 Design**                                    | ✅ **1mo Custom Development**     | 
| ✓ DB: SQLite, MySql                       | ✅ `OAuth` for Github                                                | ✅ **Team**: PM, Developer, Tester        |
| ✓ DB Tools: ORM, Flask-Migrate            | ✅ `Extended User Model`                                             | ✅ Weekly Sprints                 |
| ✓ Session-Based authentication            | ✅ `Users Roles`                                                     | ✅ Technical SPECS               |
| ✓ `Docker`                                | ✅ `Private REPO Access`                                             | ✅ Documentation                  |
| ✓ `CI/CD` Flow via Render                 | ✅ **PRO Support** - [Email & Discord](https://appseed.us/support/)  | ✅ **30 days Delivery Warranty**  |
| ✓ `Free Support`                          | ✅ Deployment Assistance                                             |  -                                 |
| ---------------------------------         | ---------------------------------                                     | ---------------------------------  |
| ✓ [LIVE Demo](https://flask-datta-able.appseed-srv1.com/)  | 🚀 [LIVE Demo](https://flask-datta-able-enh.appseed-srv1.com/) `PRO` | 🛒 `Order`: **[$7,900](https://appseed.gumroad.com/l/rocket-package)** (GUMROAD) |   

![Datta Able (enhaced with dark mode) - Open-Source Seed project generated by AppSeed.](https://user-images.githubusercontent.com/51070104/176118649-7233ffbc-6118-4f56-8cda-baa81d256877.png)

<br />

## ✅ Start in `Docker`

> 👉 **Step 1** - Download the code 

```bash
$ git clone https://github.com/app-generator/flask-datta-able.git
$ cd flask-datta-able
```

<br />

> 👉 **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## ✅ Create `.env` file

The meaning of each variable can be found below: 

- `DEBUG`: if `True` the app runs in develoment mode
  - For production value `False` should be used
- `ASSETS_ROOT`: used in assets management
  - default value: `/static/assets`
- `OAuth` via Github
  - `GITHUB_ID`=<GITHUB_ID_HERE>
  - `GITHUB_SECRET`=<GITHUB_SECRET_HERE> 

<br />

## ✅ Manual Build

> Download the code 

```bash
$ git clone https://github.com/app-generator/flask-datta-able.git
$ cd flask-datta-able
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

<br />

> Start the app

```bash
$ flask run
// OR
$ flask run --cert=adhoc # For HTTPS server
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ # CMD 
$ set FLASK_APP=run.py
$ set FLASK_ENV=development
$
$ # Powershell
$ $env:FLASK_APP = ".\run.py"
$ $env:FLASK_ENV = "development"
```

<br />

> Start the app

```bash
$ flask run
// OR
$ flask run --cert=adhoc # For HTTPS server
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:5000/register`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:5000/login`

<br />

## ✅ Codebase

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- routes.py                  # Define app routes
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- routes.py                  # Define authentication routes  
   |    |    |-- models.py                  # Defines models  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |    |    |-- includes/                  # HTML chunks and components
   |    |    |    |-- navigation.html       # Top menu component
   |    |    |    |-- sidebar.html          # Sidebar component
   |    |    |    |-- footer.html           # App Footer
   |    |    |    |-- scripts.html          # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # App Dependencies
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />

## ✅ [PRO Version](https://appseed.us/product/datta-able-pro/flask/)

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

Designed for those who like bold elements and beautiful websites, **Datta Able** is the most stylish Bootstrap 5 Admin Template compare to all other Bootstrap admin templates. 
It comes with high feature-rich pages and components with fully developer-centric code. 

- `Enhanced UI` - more pages and components
- `Improved Authentication`, Password Strength Checker
- `Automatic User Suspension` on multiple failed logins
- `Extended User profile`
- `Users Management` (restricted to admins) 

![Datta Able PRO - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/170474361-a58da82b-fff9-4a59-81a8-7ab99f478f48.png)

<br />

---
[Datta Able Flask](https://appseed.us/product/datta-able/flask/) - Open-source starter generated by **[App Generator](https://appseed.us/generator/)**.
