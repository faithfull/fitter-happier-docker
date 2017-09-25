# start with a base image
FROM debian:latest

# install dependencies
ADD sources.list /etc/apt/sources.list
RUN aptitude -y update
#RUN aptitude install -y python python-dev python-pip python-psycopg2
RUN aptitude install -y python-pip python-psycopg2
RUN aptitude install -y nginx supervisor

# add requirements.txt and install
ADD requirements.txt /code/requirements.txt
RUN pip install -r /code/requirements.txt

# set working diretory
WORKDIR /code
