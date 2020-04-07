# docker-swarm-demo

### $ docker swarm init

$ docker swarm join --token <token>

$ docker stack deploy nodeapp -c docker-compose.yml

$ docker stack ls

each stack can have multiple services (services defined in compose yml file)
to see services running under specific stack

to see services running under specific stack
$ docker stack services <service> -- gives services
$ docker stack ps <service> -- gives tasks

list all services irrespective of stack (-- only works in Swarm mode)
$ docker service ls  

scale up a service
$ docker service scale <service-name>=<no. of replicas>

To list all replicas
$ docker service ps <service-name>

remove stack
$ docker stack rm nodeapp

leave swarm mode
$ docker swarm leave --force
