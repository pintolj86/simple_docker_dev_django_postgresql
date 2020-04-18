# Simple docker compose set up to use django and postgresql.

This repository is a ready to go base project to develop a basic django app, using docker compose, django and postgresql.

## Quick Steps

1. Clone the repository.
2. On the console run: 
```
  sudo docker-compose run web django-admin startproject <project_name> .
 ```
 3. Change the permissions:
 ```
  sudo chown -R $USER:$USER .
 ```
4. In settings.py Replace: DATABASES with this configuration:
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```
5. Run: 
```
sudo docker-compose up
```
6. Go to url: http:localhost:8000 and you are ready to go.
