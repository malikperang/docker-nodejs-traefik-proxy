#Docker Nodejs Traefik Proxy

This is an example of how to use Traefik as a reverse proxy and act as load balancer to NodeJS application running on the same docker network.

###Requirements

- [Docker](https://docs.docker.com/install/)

###How to Use

Build & start Traefik container independently.

```
docker-compose --project-name=traefik_web -f docker-compose.traefik.yml up -d
```

Build & start NodeJS container app

```
docker-compose up -d --build
```

Edit [/etc/host] to map the domain

```
127.0.0.1 web.traefik.test
```

Now you can visit http://localhost:8080 for Traefik Dashboard and http://web.traefik.test to see the response from the NodeJS node.

## Authors

- **Fariz Izwan** - [Github](https://github.com/malikperang)
