web: SERVER_INSTANCE=web gunicorn service.wsgi:application --workers 2 --threads 4
release: python manage.py migrate && python manage.py collectstatic --noinput
worker: SERVER_INSTANCE=worker celery -A service worker