FROM python:slim

RUN python -m pip install --upgrade pip

COPY requirements.txt requirements.txt
RUN apt-get update && apt-get install -y \
  python3-dev \
  default-libmysqlclient-dev \
  build-essential
RUN python -m pip install -r requirements.txt

RUN mkdir /web
COPY . /web

WORKDIR /web
