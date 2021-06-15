Some important points regarding docker-compose.yml:

It will build images for db, app1, app2, Nginx based on the Dockerfiles and then spin up containers from those images.

The opened port inside app1 and app2 containers are 5000 (default port used by flask), these ports will be mapped to 5001 and 5002.

The load balancer will route traffic to the appropriate application based on that port. 

The load balancer (Nginx) will expose his internal 80 port to 8080, so we can access the application from http://localhost:8080
