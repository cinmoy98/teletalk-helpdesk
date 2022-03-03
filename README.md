# teletalk-helpdesk
This Django app helps customers to submit support ticket for queries

#Installation

* Clone the repository
* Create a virtualenv
* Enable virtual environment
* pip install django
* pip install django-helpdesk
* pip install django-bootstrap4
* Download postgres from https://www.postgresql.org/download/windows/
* Install Postgres
* Launch SQL shell
* CREATE DATABASE teletalk_support_db;
* CREATE USER dev_user WITH PASSWORD 'teletalk1234'; (replace password and username)
* ALTER ROLE dev_user SET client_encoding TO 'utf8';
* ALTER ROLE dev_user SET default_transaction_isolation TO 'read committed';
* ALTER ROLE dev_user SET timezone TO 'UTC';
* GRANT ALL PRIVILEGES ON DATABASE teletalk_support_db TO dev_user;
* pip install psycopg2
* run `django-admin startproject teletalk_support`
* Copy the `url.py` and `settings.py` to `teletalk_support/teletalk_support` folder (replace them)
* Copy the `inside_virtualenv/` `forms.py`, `models.py`, `query.py`, `urls.py` to the `virtualenv/Lib/site-packages/helpdesk` folder
* Copy the `inside_virtualenv/template` folder to the `virtualenv/Lib/site-packages/helpdesk` folder (replace the folder)
* Copy the `inside_virtualenv/views` folder to the `virtualenv/Lib/site-packages/helpdesk` folder (replace the folder)
* run `python manage.py makemigrations`
* run `python manage.py migrate`
* run `python manage.py migrate helpdesk`
* run `python manage.py createsuperuser`(this will be your login username and password to app)
* run `python manage.py runserver`
* go to `127.0.0.1:8000/helpdesk`
