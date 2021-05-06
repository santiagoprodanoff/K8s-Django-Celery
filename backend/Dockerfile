FROM python:3.9.4-buster

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /usr/src/backend

COPY Pipfile Pipfile.lock /usr/src/backend/

RUN pip install pipenv && pipenv install --system --dev

COPY . /usr/src/backend/

CMD python manage.py runserver 0.0.0.0:8000