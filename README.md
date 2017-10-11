# Heroku Django POC

First attempt at creating a heroku app that runs django

## Requirements (see also: https://devcenter.heroku.com/articles/deploying-python)

- Python 3.6.1
- virtualenv (`pip install virtualenv`)
- Django (`pip install Django`)
- heroku CLI (https://devcenter.heroku.com/articles/heroku-cli)

## Running locally on Windows (OR Linux / mac equivilent when applicable)

1. `./venv/Scripts/activate` (`. venv/bin/activate`)
2. `python manage.py migrate`
3. `python manage.py createsuperuser`
4. `python manage.py runserver`
5. Navigate to local server http://localhost:8000 
6. For admin, navigate to http://localhost:8000/admin (and login with superuser)

## Deploying to Heroku

1. `heroku login`
2. `heroku create`
3. `git push heroku master`
4. First time:
 1. `heroku run python manage.py migrate`
 2. `heroku run python manage.py createsuperuser`
5. navigate to url specified by heroku

## License: MIT

## Further Reading

- [Gunicorn](https://warehouse.python.org/project/gunicorn/)
- [WhiteNoise](https://warehouse.python.org/project/whitenoise/)
- [dj-database-url](https://warehouse.python.org/project/dj-database-url/)
