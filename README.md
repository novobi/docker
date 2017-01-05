About this Repo
======

This is the Git repo of the official Docker image for [Odoo](https://registry.hub.docker.com/_/odoo/). See the Hub page for the full readme on how to use the Docker image and for information regarding contributing and issues.

The full readme is generated over in [docker-library/docs](https://github.com/docker-library/docs), specifically in [docker-library/docs/odoo](https://github.com/docker-library/docs/tree/master/odoo).

[Jan 05, 2017] Add ODOO_PORT environment. Odoo instance will run on ODOO_PORT instead of default port 8069.

Docker build:
`$ docker build . -t novobi:odoo10`

Docker run:
`$ docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo --name db postgres:9.4`
`$ docker run -p 8090:8090 -e ODOO_PORT=8095 --name odoo --link db:db -t novobi:odoo10`