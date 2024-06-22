# DOCKER

``
In darker ages
one application on one
physical server


APPLICATION
----------------
OS
----------------
PHYSICAL SERVER


--> slow deployment times
--> huge costs
--> difficult to scale 
and migrate
--> Wasted resources


# HYPERVISOR based
# VIRTUALISATION

--> one 
physical server can contain multiple applications
-- Each application runs in a virtual machine

APPLICATION | APPLICATION | APPLICATION
--------------------
HYPERVISOR
------------
HOST OPERATING SYSTEM
----------
PHYSICAL SERVER

Each VM still requires
--CPU allocation
-- RAM
-- STORAGE
--> AN entire guest OS

--> CONTAINERIZATION virtualization

# standardized packing for software and dependencies 
# ISOLATE and dependencies
# Isolate apps from each other
# Share the OS level


# CONTAINERS ARE AN APP LEVEL CONSTRUCT

CTr1      | CTr2   
APP A     | App B
Bins/libs | Bins/lib

--------------
DOCKER
--------------
HOST OS
--------------
INFRASTRUCTURE

# VMs are an infrastructure
level Construct to turn
one machine to many servers


Containers and VMs provide tremendous 
amount of flexibility for IT to optimally deploy and manage apps

> DOCKER IMAGE
`The basis of a docker container`
								``

> DOCKER CONTAINER
The image when it's running.
The standard unit for app service
                                ``

> DOCKER ENGINE
The software that executes commands for containers.
Networking and Volumes are part of
Engine. 
                                  ``

> DOCKER REGISTERY
Stores, distributes and manages Dockerimages
                                   ``

> Control Plane
Management Plane for container and 
Cluster Orchestration

<!-- IMAGE LAYERS -->
Images are comprised of multiple layers  
Every image contains a base layer
A layer is also just another image
Docker uses a copy on write system
Layers are read only


# DOCKER SEARACH IMAGE_NAME
to search image in dockerhub
registery

# DOCKER RUN IMAGE_NAME
to make image container 

# DOCKER PS 
to check containers ( running)

# DOCKER PS -a
to check containers (running as well
as stopped/exited)

# DOCKER run -dt /-it  IMAGE_NAME
to run/make containers in deattached
mode so that they work effectively

# DOCKER EXEC -IT IMAGE_NAME /BIN/BASH
to enter inside the container

# DOCKER RUN --PUBLISH / -p 90:90
to connect the ports of the machine and containers 

# DOCKER RUN -P 
to connect automatically port selection [capital P]


# DOCKER IMAGE INSPECT IMAGE_NAME
to see details about image

# DOCKER INSPECT CTR_NAME
to see details about container

# DOCKER SYSTEM PRUNE 
This will remove
all stopped containers
all networks not used by at least one container
all dangling images
all dangling build cache 


# DOCKER --name 
To set the name of the docker machine

# DOCKER -v /folder : /folder
To attach system folder with container folder. 

# DOCKER STOP $(docker ps -q)
To stop all running containers

# DOCKER RM $(docker ps -a -q)
TO remove all running containers

# DOCKER RMI $(docker images -a -q)
to delete all docker images

# DOCKER RM $(DOCKER PS -a -f status=exited) -q
To remove all exited containers

# DOCKER STATS CONTAINER_NAME
To see the statistics of a container
