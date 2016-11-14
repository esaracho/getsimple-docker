# getsimple-docker

# Building the container:

sudo docker build -t mysite .

# Unzip GetSimple in your dev directory and change owner (apache):

unzip GetSimple.zip myweb/
chown -R www-data:www-data myweb/

# Run Docker:

sudo docker run -p 8080:80 -v /path/to/myweb:/var/www/site mysite
