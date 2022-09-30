FROM python:3.8.slim-buster

WORKDIR /app

COPY ./requirements.txt ./requirements.txt
RUN python -m pip install -r requirements.txt

COPY . /app

EXPOSE 5000

CMD ["gunicorn", "-c", "config.py", "--bind", "0.0.0.0:5000", "app:app"]
