# Deploying on dokku

[Dokku](https://github.com/progrium/dokku) is a Docker powered mini-Heroku in around 100 lines of Bash.

If you’re familiar with using git in the command line, you’ll have no trouble deploying your Harp app to Dokku.

## Setup a dokku environment

You can install Dokku on your own by following the instructions [here](https://github.com/progrium/dokku#requirements) or another approach is using a DigitalOcean [dropplet](https://www.digitalocean.com/community/tutorials/how-to-use-the-digitalocean-dokku-application).

## Setuping a development environment

**Requirements:** git, node 0.10.x, npm 1.2.x

### 1. Setting up the remote repo

Clone this repo to your location machine `git clone https://github.com/subhaze/hb-dokku.git <your_app_name>` then `cd <your_app_name>` into the folder you cloned to and setup the remote repo, which should be something like: `git remote add dokku dokku@<your_domain>:<your_app_name>`

### 2. Running locally

If you have harp installed globally `npm install -g harp` you can start up the harp server via `harp server`. If you don't have harp setup you can run `npm install` to install it locally and then you can start up the app via `node_modules/.bin/harp server`

### 3. Deploying your app

Now all you have to do is commit any changes you've made then `git push dokku master` and you've just deployed your [harp](http://harpjs.com/) app!
