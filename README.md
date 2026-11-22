# Todo list API

Django REST framework API (users and groups), generated with Django 3.1.

## Run locally

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

Edit `.env` and set `SECRET_KEY` to a long random value:

```bash
python -c "import secrets; print(secrets.token_urlsafe(50))"
```

Then:

```bash
python manage.py migrate
python manage.py runserver
```

A `.env` file in the project root is loaded for local development and is not committed. Existing environment variables take precedence over `.env`.

| Variable | Purpose |
| --- | --- |
| `SECRET_KEY` | Required. Django signing key. |
| `DEBUG` | `True` or `False`. Defaults to `False` when unset. |
| `ALLOWED_HOSTS` | Comma-separated hostnames, for example `localhost,127.0.0.1`. |

Django 4.2 runs this project on current Python. The original code was generated with Django 3.1.
