Docker PHPMyAdmin
=================

Forked from https://github.com/corbinu/docker-phpmyadmin to remove the database login for convenience (but not security!)

## Start a MySQL server container

This uses the https://hub.docker.com/_/mysql/ base container.

`docker run --name phpmyadmin-mysql -e MYSQL_ROOT_PASSWORD=password -d mysql`

## Start PHPMyAdmin (this container)

`docker run -d --link phpmyadmin-mysql:mysql -e MYSQL_USERNAME=root --name phpmyadmin -p 80 ahebrank/phpmyadmin`
