FROM python:3.8-slim

# layer caching for faster builds
COPY requirements.txt /
RUN pip install -r /requirements.txt

#COPY app.py /app.py
ADD . /celery-beat
WORKDIR /celery-beat

ENTRYPOINT celery --app app beat --loglevel=INFO --max-interval 10
