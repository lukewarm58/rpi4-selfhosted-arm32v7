# rpi4-selfhosted-arm32v7
A collection of docker-compose files used with my 2GB Raspberry Pi 4.

Inspired by the [novaspirit pi-hosted](https://github.com/novaspirit/pi-hosted) project, [DB Tech](https://www.youtube.com/c/DBTechYT), [GeekedTV](https://www.youtube.com/c/geekedtv), [Techno Tim](https://www.youtube.com/c/TechnoTimLive) and [Awesome Open Source](https://www.youtube.com/c/AwesomeOpenSource/).

Having become a little more familiar with portainer and docker-compose, I have started to prefer bringing up docker containers from the command line. I still like to have Portainer installed though.

**Notes:** 
- At the time of writing this, I am running Debian (Buster) 10.11
- `cat /etc/os-release`  and `cat /etc/debian_version`
- Because of the operating sytem I am running, I need to pull arm32-v7 compatible docker images from [Docker Hub](https://hub.docker.com/)
- My RPi OS is on a 250GB SSD connected to the Pi using a SATA to USB adapter 
- I have assigned a fixed IP address to my Pi using my router's software (192.168.x.x)
- Unless things change, everything I run is only available to devices connected to my home network
- I use the simple folder structure `/home/pi/docker/*program*` to store the `docker-compose.yml`, persistant data, and any other required files for each application

### List of Self-Hosted Programs
- [Nullboard](https://github.com/apankrat/nullboard) :: A minimalist take on a kanban board
  - *A super beautiful and useful application, the fact that its data is tied to your web browser and not the RPi server led me to find an alternative kanban/to-do application*
  - I used a mashup of the [apankrat](https://github.com/apankrat/nullboard) and [rsoper](https://github.com/rsoper/nullboard) projects
  - Inside `/home/pi/docker/nullboard/` are the files `docker-compose.yml` and `Dockerfile` plus a folder called `app`
  - I used the `nullboard.html` file from [apankrat](https://github.com/apankrat/nullboard) and renamed it index.html as per the [rsoper](https://github.com/rsoper/nullboard) fork
  - I populated the `/home/pi/docker/nullboard/app/extras` folder with the files inside the `extras` folder of [apankrat](https://github.com/apankrat/nullboard)
- [Planka](https://github.com/plankanban/planka)
- [Vikunja](https://github.com/go-vikunja/api)
- [NocoDB](https://github.com/nocodb/nocodb)


