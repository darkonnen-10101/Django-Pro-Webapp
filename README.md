## Start Djangop project

django-admin startproject codedaddies_list

## Manage enviroment

conda create --name codedaddies_list

conda activate codedaddies_list

## Run server

python3 manage.py runserver

## Make migrations

python3 manage.py makemigrations

## Commit migrations

python3 manage.py migrate

## Create Admin interface

python3 manage.py createsuperuser

## After model created

python3 manage.py makemigrations

## Commit model migrations

python3 manage.py migrate

## Deplyment

> created Procfile in root and added config
> Edited settings.py in main

pip3 install django-heroku
pip3 install heroku
pip3 install psycopg2
pip install gunicorn
pip3 freeze > requirements.txt

heroku login
heroku create

[Medium post tutorial - Django heroku deployment](https://medium.com/@qazi/how-to-deploy-a-django-app-to-heroku-in-2018-the-easy-way-48a528d97f9c "Tutorial Django Heroku Deployment")

heroku addons:create heroku-postgresql:hobby-dev
heroku run python manage.py migrate

git add .
git commit -m "{{Message}}"
git push heroku master
