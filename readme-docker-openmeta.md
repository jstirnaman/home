# Instructions:
https://hub.docker.com/r/opencpu/centos6/
https://github.com/jeroenooms/opencpu-server/tree/master/docker#readme
# Run Rstudio in first terminal
docker run -it -p 80:80 -p 8004:8004 -v /Users/jts558/openmetaanalysis-r:/home/openmeta -P opencpu/rstudio 

# Restart rstudio-server
docker exec {container_name} /bin/sh -c 'rstudio-server restart'

# Run bash in second terminal
docker exec -it {container-name} bash

# OR start with an interactive shell
docker run -t -i -p 80:80 -p 8004:8004 opencpu/rstudio /bin/sh -c '/bin/bash'
docker-machine ssh docker-vm

sudo iptables -t nat -L -n

# Load a local library
$ R
> install.packages("/home/openmeta/home")
