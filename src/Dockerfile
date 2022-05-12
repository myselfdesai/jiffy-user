# pull official base image
FROM python:3.6-alpine

# set work directory
WORKDIR /usr/src/app

# # copy requirements file
COPY ./Pipfile /usr/src/Pipfile

# install dependencies
RUN pip install --upgrade pip && \
    pip install pipenv

# copy project
COPY . /usr/src/app/

RUN pipenv install --system --deploy --ignore-pipfile