# DOCKER
- What's docker?
docker is aplatform for building ,running and shipping applications.it works on all machines.
if ur application works on your development machine and doesn't  somewhere
# REASONS
- One or more files are missing
- software version mismatch eg when ur development machine is using node 14,but the target machine is using node 9.
- Different configuration settings eg environment varriables are different across these machines.
with docker you can easily  package ur application with everything it needs and run it anywhere on any machine with docker.
if your application needs a given version of packages ;
### Node 14
### mongo 4
 app,all of these would be included in the application package and run it on any machine that runs docker.
 if someone joins ur team,they don't have to spend half aday setting up their machines to run your application ,they don't have to install and configure all these dependencies.
 They simply tell docker to compose up and docker itself will automatically dowload and run these dependencies inside an isolated enviroment called a container,this isolated enviroment allows multiple and different version of software eg node 14,node 9,app1 and app2 side by side in the same machine without messing each other.
 when ur done with the application u can remove it with it's dependencies in one go,using the command
 # docker-compose down --rmi all
 so docker consistence is built,run and ship application.
 
 
#  virtual machines vs containers
## containers
An isolated enviroment for running an application
## virtual machine
An abstraction of a machine (physical hardware) for eg we can have mac ,we have two virtual machines,one running windows and other running linux using a tool called a hypervisor.
## Hypervisors
- virtual box
- vmware
- Hyper-v(windows only)
with hypervisor,we can manage virtual machines
we can have two vitual machines runing different apps,say app1 and app2,app1 may use node 14 and mongo4 and app2 may use node 9 and mongo 3,all these are runing on the same machine but different isolated enviroments,this is one of the advantages of virtual machines.
## problems
- Each virtual machine needs a full-blown os(operating systems)
- slow to start
- Resource intensive in terms of memory,pysical hardware,processor
## Advantages of containers
- Allow runing of multiple apps in isolation
- Are lightweight
- They use the os of the host
- Start quickly
- Needs less hardware resources

# Architecture of docker
docker uses aclient server architecture,the client communicates to the server using the rest API,containers are just aprocess,all containers share the kernel of the host,kernel is the core of an operating system.
A kernel manages applications and hardware resources like memory and cpu.
# installation of docker on linux
dowload the latest version 20.10.5

# Development workflow with docker
instructions
- start with an os
- install node
- copy app files
- run node app.js
