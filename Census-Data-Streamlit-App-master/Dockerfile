FROM python:3.8-slim-buster

ENV VAR1=10

ENV PYTHONDONTWRITEBYTECODE 1

ENV PYTHONUNBUFFERED 1

COPY . /app
WORKDIR /app

EXPOSE 80

RUN python -m pip install -r requirements.txt

RUN mkdir ~/.streamlit
RUN cp config.toml ~/.streamlit/config.toml
RUN cp credentials.toml ~/.streamlit/credentials.toml
WORKDIR /app

ENTRYPOINT ["streamlit", "run"]
CMD ["census_app.py"]