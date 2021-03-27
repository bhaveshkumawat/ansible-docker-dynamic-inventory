# docker-dynamic-inventory
Firstly as the playbook launched we are asking for the name of container to be launched.

Docker repo- This is the task in which the repository for yum is being configured which will be used for downloading the docker.

Installing docker- through this the docker will be installed on the managed node.

Starting docker service- this task is for starting the services of docker engine.

Installing docker-py- in this task the required sdk for the docker will be installed with the help of pip3 command .

Pulling image for docker container- this task is used to pull the required image for launching the container.

Creating  a docker container- this task will launch the docker container with the name specified and the image pulled.

Retrieving the ip-in this task the all details of the container launched will be stored in the variable var and to get ip from this we have to use it  as:-

var.container.NetworkSettings.IPAddress

Configuring the ip- in this task an inventory file will be created using blockinfile module of ansible.

NOTE:-  The file will be created inside the managed node so we have to find a way to get this file from the managed node to our controller node of ansible.

Getting inventory file- in this task the module used is ansible.builtin.fetch module through this we can download the inventory file created in the managed node to our own system(i.e. Controller node).
