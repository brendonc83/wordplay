Demo
-----

[Live Site (hosted on Heroku)](https://word-play.herokuapp.com)

Setup
-----

```
virtualenv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Testing
-------

```
export TEAMTEMP_SECRET_KEY=`python -c 'import uuid; print uuid.uuid4()'`
export DJANGO_SETTINGS_MODULE=wordplay.settings
export DATABASE_URL=sqlite:///`pwd`/wordplay.sqlite
python manage.py test
```

Coverage
-------

```
coverage run manage.py test
coverage report -m
```

Running
-------

```
python manage.py migrate
python manage.py collectstatic
python manage.py runserver
```

Build Health
-----------
[![Build Status](https://travis-ci.org/mvillis/wordplay.svg)](https://travis-ci.org/mvillis/wordplay)
[![Coverage Status](https://coveralls.io/repos/mvillis/wordplay/badge.svg?branch=master&service=github)](https://coveralls.io/github/mvillis/wordplay?branch=master)
