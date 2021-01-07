# Django Example: https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application
## Create virtual environment
python -m venv venv
## Activate (Linux)
source venv/bin/activate
## Activate (Windows)
venv\Scripts\activate
## Add gunicorn (HTTP server) and Martor (Markdown plugin for Django) to project
echo martor >> requirements.txt
echo gunicorn >> requirements.txt

## migrations
python manage.py makemigrations
python manage.py migrate






docker run -it -p 8020:8020 -e DJANGO_SUPERUSER_USERNAME=admin -e DJANGO_SUPERUSER_PASSWORD=sekret1 -e DJANGO_SUPERUSER_EMAIL=admin@example.com django-markdown-editor




note to not autoconvert LF to CRLF with git
	git config --global core.autocrlf false