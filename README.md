## Routing Proxy

This project works as a routing proxy for a system of multiple docker-compose projects running on one domain, that are accesible through various subdomains.

Every project has to listen on a different port. This proxy then listens to port 80 and intercepts all trafic.

For the other projects to be visible to this proxy, their containers (at least one) must be part of docker a network.

````
networks:
  routing_proxy:
    name: routing_proxy
````
