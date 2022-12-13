# Docker Without Cookiecutter
    In this repo we try to do practical on docker creating dockerfile only.

## PreRequsite :

    - Software which you have to install : 
             1. docker-desktop 	
             2. git 

    - If you are working on VSCode install extension : 
             1. docker

    - If you have seeing error in :
             1. Click on the given link : https://aka.ms/wsl2kernel and install this software.
             2. When page open just look for STEP 4: DOWNLOAD THE LINUX KERNEL UPDATE PACKAGE  where you get this link click on it and download 
             3. https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi 

    - Create your docker account on : https://www.docker.com/

## Install Requirements :
    pip install -r requirements.txt

## How to check docker is installed and ready for work or not:
    - In vs code terminal type : docker login (if you logged in then it’s working)
    - In cmd type : docker –verson (if you saw version you can now ready to work)
 
## Step To Setup Your Docker:
    Create your django projects as you in general create. Only add 3 files at project level
        1- Dockerfile 	
        2- command.txt	
        3- .dockerignore

## In dockerfile Mention : 
    FROM python:3.8-slim-buster
    WORKDIR /app
    COPY requirements.txt requirements.txt
    RUN pip3 install -r requirements.txt
    COPY . .
    CMD ["python","manage.py","runserver","0.0.0.0:8000"]

## Command to Run Docker:
    1. docker build --tag python-django .
    2. docker run --publish 8000:8000 python-django

### Refrence : 
[Blog](nahid-ibne-akhtar.medium.com/django-app-on-docker-or-dockerize-your-existing-django-app-on-windows-10-be4c28937dc)

<a href="https://www.youtube.com/watch?v=W5Ov0H7E_o4">Youtube Link</a>

<a href="https://docs.google.com/document/d/1yClbE24tpVuEaNYpljbb1L0Wwio7Mz5Aj4P8Uk7NrZ4/edit?usp=sharing">Google Doc </a>