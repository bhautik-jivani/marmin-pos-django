# syntax=docker/dockerfile:1
FROM python:3

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /marmin_pos

COPY requirements.txt /marmin_pos/

RUN pip install -r requirements.txt

COPY . /marmin_pos/

RUN mkdir -p /var/log/gunicorn
RUN chown -R 777 /var/log/gunicorn

RUN mkdir -p /var/log/nginx
RUN chown -R 777 /var/log/nginx