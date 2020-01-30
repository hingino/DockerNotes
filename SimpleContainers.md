## Containers

You can use conainers in 3 different ways.
1. To run a single command
2. Running run as a shell
3. Running in the background

#### 1. Running as a single command
    docker container run [options] [image:version] [hostname]

#### 2. Run as shell
    docker container run --interactive --tty [options] [image:version] [shell]
* `--interactive` says you want an interactive session
* `--tty` allocates a pseudo-tty
* `[shell]` is the command to run your shell of choice

#### 3. Run in background
    docker container run --detach --name [name] [options] [image:version]
* `--detach` runs container in background
* `--name [name]` sets the name of the container

Although this contianer is running the background, you still have the ability push commands to the container or even open a shell
    docker exec -it [name] [command]
* to start a shell, make your command your prefered shell

#### Other Container Stuff
* List Running Containers `docker container ls`
* List all containers reguardless of status `docker container ls -a`
* Show logs `docker container logs [name]`
* Show running processes `docker container top [name]`