# syntax=docker/dockerfile:1

FROM ubuntu:20.04

WORKDIR /root

RUN apt update
RUN apt install -y python3
RUN apt install -y python3-pip
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]