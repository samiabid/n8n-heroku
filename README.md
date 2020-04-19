# n8n-heroku

### n8n(Nodemation) - Free and Open Workflow Automation Tool

This is a heroku focused container implementation for the [n8n Automation Tool]. Just connect your fork of this repo to heroku and let it work as a charm!

## Requirements
* Heroku CLI

## Setup

you need to prepare your heroku app before deploying this project. given below in 3 simple steps!

### STEP 1: CHANGE your App Stack to container
you can change your app's stack using heroku cli, make sure you have heroku cli installed.

#### login into heroku account
    heroku login

#### change app stack
    heroku stack:set contaner --app APP_NAME
replace APP_NAME with your heroku app name

### STEP 2: ADD Config Vars for enabling basic authentication (Optional)
It's recommended that you enable basic authentication when deployingn n8n on web. You need to set the following Environment Variables(Config Vars) in your App settings.

    N8N_BASIC_AUTH_ACTIVE=true
    N8N_BASIC_AUTH_USER=SET_USERNAME
    N8N_BASIC_AUTH_PASSWORD=SET_PASSWORD

### STEP 3: DONE! Now CONNECT Github repo and Deploy.

## Using Container Registry

you can also deploy this project using container registry (requires aditional requirements installed). Just clone/download this repository on your local machine.

### Additional Requirements (for building on local)
* docker
* docker-compose

### Steps
cd into your project directory

    cd n8n-heroku/

build and push container image to heroku

    heroku container:push web --app APP_NAME
    
release

    heroku container:release web --app APP_NAME


[n8n Automation Tool](https://n8n.io/)