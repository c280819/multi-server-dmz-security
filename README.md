# multi-server-dmz-security
A secure multi-server architecture deployed within a DMZ, integrating web, database, and mail servers with firewall, SSL, and monitoring for enhanced network protection.

## Overview
This project demonstrates a **multi-server architecture** deployed within a **DMZ (Demilitarized Zone)** to enhance network security. It integrates multiple servers such as Web Server, Database Server, and Mail Server with security tools, monitoring, and intrusion detection.

## Features
- Secure multi-server setup within DMZ
- Flask web application deployment
- Mail server & webmail setup
- Monitoring & intrusion detection
- UFW firewall configuration

## Project Structure
multi-server-dmz-security/

├── webserver/

│ ├── app.py

│ ├── requirements.txt

├── dbserver/

│ ├── mariadb-setup.sql

│ └── config/

├── mailserver/

│ ├── postfix-config/

│ └── dovecot-config/

├── ssl-certificates/

│ ├── todo.sunbeam.local.pem

│ └── todo.sunbeam.local-key.pem

└── README.md

## Prerequisites
- Debian 12
- Python 3.10+
- Docker (optional)
- Internet connection for package installation

## Setup & Installation

1. **Clone the repository**
```bash
git clone https://github.com/c280819/multi-server-dmz-security.git
cd multi-server-dmz-security

Web Server setup

cd webserver
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py


Database Server setup

cd ../dbserver
# Import MariaDB setup
sudo mysql -u root -p < mariadb-setup.sql


Mail Server setup

cd ../mailserver
# Follow postfix and dovecot configuration steps


Access

Web application: https://todo.sunbeam.local:5000

Database: MariaDB server

Mail: Webmail interface
