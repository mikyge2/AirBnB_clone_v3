# AirBnB Clone - Version 3

## Overview

This repository contains version 3 of the **AirBnB clone** project, a simplified full-stack clone of the AirBnB web application. This version builds upon previous iterations and introduces RESTful APIs, dynamic content handling, and enhanced deployment scripts.

### Project Goals

* Implement RESTful APIs using Flask
* Manage MySQL database interactions
* Package static content
* Automate deployment via shell/Python scripts
* Structure a modular and scalable codebase

---

## Directory Structure

```
.
├── api/                    # RESTful API routes
├── dev/                    # Development environment configurations
├── etc/                    # Configuration files for web servers (e.g., nginx)
├── models/                 # Data models (e.g., User, Place, City)
├── tests/                  # Unit and integration tests
├── web_flask/              # Flask web application logic
├── web_static/             # Static content (HTML, CSS, JS)
├── wsgi/                   # WSGI entry points for deployment
├── 0-setup_web_static.sh   # Initial static setup script
├── 1-pack_web_static.py    # Script to create .tgz archive of web_static
├── 2-do_deploy_web_static.py # Deployment script to distribute archive
├── 3-deploy_web_static.py # Complete deployment pipeline
├── AUTHORS                 # Contributors
├── LICENSE                 # Licensing info
├── README.md               # Project overview and instructions
├── code_review.txt         # Peer code review notes
├── console.py              # Entry point for command interpreter
├── git.sh                  # Git automation script
├── requirements.txt        # Python dependencies
├── setup_mysql_dev.sql     # SQL script to setup dev DB
├── setup_mysql_test.sql    # SQL script to setup test DB
```

---

## Features

* **RESTful API** for CRUD operations
* **MySQL database** integration
* **Modular codebase** for scalability and clarity
* **Shell and Python scripts** for packaging, deployment, and server setup
* **Test coverage** for reliability

---

## Technologies Used

* Python 3
* Flask
* MySQL
* SQLAlchemy
* Gunicorn + Nginx (for deployment)
* Bash scripts

---

## Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/mikyge2/AirBnB_clone_v3.git
cd AirBnB_clone_v3
```

2. **Create a virtual environment & install dependencies**

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

3. **Setup MySQL DB**

```bash
cat setup_mysql_dev.sql | mysql -u root -p
```

4. **Run API locally**

```bash
python3 -m api.v1.app
```

5. **Start the console (CLI tool)**

```bash
./console.py
```

---

## Deployment

You can automate deployment using the provided scripts:

```bash
./0-setup_web_static.sh         # Prepares the web server
python3 1-pack_web_static.py    # Packages web_static
python3 2-do_deploy_web_static.py <archive_path>   # Deploys the archive
python3 3-deploy_web_static.py  # Full pipeline
```

---

## Contributors

See `AUTHORS` file for full list of contributors.

---

## License

This project is licensed under the terms of the MIT License. See the LICENSE file for more details.

---

## Acknowledgments

This project is inspired by the AirBnB project from the Holberton School curriculum. It is an educational exercise to learn full-stack development principles, infrastructure automation, and API design.
