# hello-vue + Django

This is a boilerplate project for using vuejs with Django.

### Features

* Django backend in `./backend`
* vuejs (v2) frontend in `./frontend`
* Hot-reload with vue-loader
* eslint linter integration
* Makefile to make your life easy


### Development environment setup

These steps will install all required dependencies including development ones, run migrations and start dev server.

Decide on a projectname

```bash
git clone this repository
rename the hello-vue-directory to your project_name
cd project_name
update the project name in the package.json
mkvirtualenv --python=/usr/bin/python3 [project_name]
pip install --upgrade pip
make dev
make migrate
# note that it is manage, not manage.py
python manage createsuperuser
make run
```
### now change the git repo

```bash

create a new repo at git, use appropriate name 

# list the current repo
git remote -v
# make a new repo
git remote set-url origin https://github.com/eezis/[repo_name_here]
```

### Deployment

These steps will install productio dependencies and build vuejs application to `static/dist` folder.

```bash
make prod
make build
```

### Be aware

For the sake of simplicity Django config is contained within it's own backend app. In real world setting you would
probably want to remove `backend` from `INSTALLED_APPS`, create a new app and move `backend.views` to it.

You probably want to create python virtual environment as well. Default python instance available will be used.
