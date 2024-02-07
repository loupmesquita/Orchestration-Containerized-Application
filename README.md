# Orchestration-Containerized-Application
## Deployment of an application to a multi-host cluster using Kubernetes. <br/> <br/>

Traefik is used as a reverse proxy and load balancer. <br/>
The application is a simple web poll application. <br/>
There are five elements constituting the application: <br/> <br/> 
- Poll, a Flask Python web application that gathers votes and push them into a Redis queue. <br/>
- A Redis queue, which holds the votes sent by the Poll application, awaiting for them to be consumed by
the Worker. <br/>
- The Worker, a Java application which consumes the votes being in the Redis queue, and stores them into
a PostgreSQL database. <br/>
- A PostgreSQL database, which (persistently) stores the votes stored by the Worker. <br/>
- Result, a Node.js web application that fetches the votes from the database and displays the result. <br/>

![image](https://github.com/loupmesquita/Orchestration-Containerized-Application/assets/57537562/f0d681aa-f75e-4d84-bdc7-9f544f2a3842)
