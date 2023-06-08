# Simple blog
Frontend is made with VueTS 3 + Vite. Backend is made in Node TS + Express with Sequelize ORM, and JWT. Project supports docker multi-stage build for development and production.

# Prerequisites
`Docker` and `DockerCompose` should be installed on your device and you have access to the `root` user, for running docker.

# Installation
```
# get the main repository
git clone https://github.com/gushi-cookie/simple-blog.git

# come to the project directory
cd simple-blog

# create 'services' directory and get in
mkdir services && cd services

# get repositories of the services
git clone https://github.com/gushi-cookie/simple-blog-nginx.git nginx
git clone https://github.com/gushi-cookie/simple-blog-frontend.git frontend
git clone https://github.com/gushi-cookie/simple-blog-backend.git backend

# go to the root of the project and fill up an environment file
cd ../
cp .env.example .env
nano .env

# then build the project
sudo docker-compose build

# and start services
sudo docker-compose up
```
Result can be seen on `localhost:80`.