# Cloud-computing-
Concepts of cloud computing, basics, related topics details 

![Screenshot_2024_0918_123427](https://wallpaperbat.com/img/1301774-cloud-computing-wallpaper.jpg)

# Cloud Computing:- 

Cloud computing is the provision of computing services over the Internet, or "the cloud." These services include servers, storage, databases, networking, software, analytics, and intelligence, enabling faster innovation, resource flexibility, and cost efficiencies at scale.

![Screenshot_2024_0918_123503](https://www.infosectrain.com/wp-content/uploads/2023/07/architecture-of-cloud-computing-.jpg)
# Docker:- 

Docker is a software platform designed to facilitate the rapid building, testing, and deployment of applications. It packages software into standardized units known as containers, which include everything needed for the software to run, such as libraries, system tools, code, and runtime. With Docker, you can deploy and scale applications across any environment with confidence that your code will operate consistently.

![Screenshot_2024_0918_124023](https://jfrog.file.force.com/servlet/servlet.ImageServer?id=01569000008kqFT&oid=00D20000000M3v0&lastMod=1631619825000)
 
 # Key features of Docker include:-

# 1.Containerization: 
Applications run in isolated environments, making them portable and straightforward to manage.

# 2. Images and Dockerfile: 
Docker uses images as templates for creating containers. A Dockerfile is a script with a set of instructions to build an image.

# 3. Docker Hub:
A cloud-based registry enables users to store, share, and distribute Docker images.

# How Docker works:- 

Docker functions by providing a standardized way to execute code. It acts as an operating system for containers, similar to how a virtual machine virtualizes hardware. Containers, however, virtualize the server’s operating system. With Docker installed on each server, you can use straightforward commands to build, start, or stop containers.
![Screenshot_2024_0918_123713](https://phoenixnap.com/kb/wp-content/uploads/2024/01/container-vs-virtual-machine-what-is-docker.jpg)

# What is the structure of a Docker image?:- 

A Docker image is composed of multiple layers stacked on top of each other. Each layer represents a specific modification to the file system (inside the container), such as adding a new file or modifying an existing one. Once a layer is created, it becomes immutable, meaning it can't be changed.

![Screenshot_2024_0918_124113](https://media.geeksforgeeks.org/wp-content/uploads/20221205115118/Architecture-of-Docker.png)


# HOW TO INSTALL DOCKER:- 

To install Docker on a remote server using PuTTY, you'll first need to ensure you have access to a Linux server (like Ubuntu, CentOS, etc.) via SSH. Here's a step-by-step guide:

## Step 1:Connect to Your Server


## Step 2: Update Your Package Index

Before installing Docker, it’s a good idea to update the package index:

```bash
sudo apt update
```


## Step 3:Install Prerequisites

For Ubuntu, install the required packages:

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

For CentOS, run:

```bash
sudo yum install -y yum-utils
```

## Step 4: Add Docker’s Official GPG Key

For Ubuntu:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

For CentOS:

```bash
sudo rpm --import https://download.docker.com/linux/centos/gpg
```

## Step 5: Set Up the Stable Repository
For Ubuntu:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```


For CentOS:

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

## Step 6: Install Docker

For Ubuntu:

```bash
sudo apt update
```

```bash
sudo apt install docker-ce
```

For CentOS:

```bash
sudo yum install docker-ce
```

## Step 7: Start Docker

Enable and start the Docker service:


```bash
sudo systemctl start docker
```

```bash
sudo systemctl enable docker
```

## Step 8: Verify the Installation

Check if Docker is running:

```bash
sudo systemctl status docker
```

You can also run a test container:

```bash
sudo docker run hello-world
```

## Step 9: (Optional) Manage Docker as a Non-Root User

If you want to run Docker commands without sudo, add your user to the 

Docker group:

```bash
sudo usermod -aG docker $USER
```

After running this command, log out and back in for the changes to take effect.

# Conclusion

You’ve successfully installed Docker using PuTTY! If you have any questions or run into issues, feel free to ask.

# container:-

Containers are a lightweight way to package and deploy applications, bundling code and dependencies into a single unit. This approach allows multiple containers to run concurrently on a single machine, sharing the operating system kernel and running as isolated processes in user space. As a result, containers offer several key benefits:

They are much smaller in size, typically ranging from tens of megabytes to a few gigabytes.
They can support a higher number of applications compared to traditional virtual machines.
They require fewer virtual machines and operating systems, making them a more resource-efficient option.

![Screenshot_2024_0918_124201](https://www.docker.com/wp-content/uploads/2021/11/docker-containerized-and-vm-transparent-bg.png)

# NGINX:-

NGINX is a popular, high-performance web server and reverse proxy server that excels at serving web applications and handling HTTP and HTTPS requests. Its key strengths include:

Speed and efficiency: NGINX is designed to handle a large number of concurrent connections with minimal resource usage.

Scalability: It can efficiently distribute traffic and handle load balancing, making it a reliable choice for high-traffic web applications.

![Screenshot_2024_0918_140523](https://github.com/user-attachments/assets/ff5971c8-d6b8-434e-b93a-8476dc5a8f83)

# HOW TO INSTALL NGINX :-
In this tutorial, we’ll show you how to install NGINX on Linux.

## Open your Linux machine and run an update using the command below:

```bash
sudo apt-get update
```

Next, run this command:

```bash
sudo apt-get install nginx
```

## Then, enable your firewall with the following:

```bash
sudo ufw enable
```

## To verify NGINX is installed, run the following:

```bash
nginx -v
```

## You can run the command below to find out if NGINX is running:

```bash
sudo ufw status
```

After running this command, you should see the following:

status: active

## To check whether your NGINX server is working fine, run the following:

```bash
sudo systemctl status nginx
```

# using EC2 in AWS:-

First open AWS search EC2 then Launch Instance and there select keypair in putty then download it

after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

## after that run it and write username as ubuntu as selected os and then type following commands

```bash
sudo apt update
```


```bash
sudo apt install apache2
```

## to install a web server on ip then

```bash
sudo su
```

## for convert $ into # for getting admin role then

```bash
cd /var/www/html/
```

##then

```bash
ls
```

## for list of html file in it

## then copy that html file name and write

```bash
rm index.html
```

```bash
rm means remove command
```

```bash
vi index.html
```

this will open a notepad like and write html code there like (vi is editor) -

then press ctrl+c then shift+colon then write wq and enter

now copy your public ip and paste it on browser you will see the texts written by you (by using html above)



# USING CONTAINER IN VM and adding nginx server by Docker:- 

First open AWS search EC2 then Launch Instance and there select keypair in putty then download it

after that edit network setting and click on add security group rule and select TCP,UDP,ALL TRAFFIC AND SELECT EVERYWHERE SOURCE TYPE IN THEM then Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH 


(SSH (Secure Shell) is a way to securely connect to another computer over a network. It's like a safe tunnel that allows you to control a remote computer and transfer files to it, without anyone else being able to listen in or interfere with the connection.)

then Auth then Credentials and open there

after that run it and write username as ubuntu as selected os and then type following commands

```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

## this will install and run docker in your vm

```bash
newgrp docker
```

## this command will help us to use docker

```bash
docker ps
```

## this will list docker

```bash
docker --version
```

## this will display the version of docker installed

## now installing nginx

```bash
docker pull nginx
```

## You can download Nginx from a pre-built Docker image, with a default Nginx configuration, by above command. This downloads all the necessary components for the container.

```bash
docker run --name docker-nginx -p 80:80 nginx
```

Nginx installed, you can configure the container so that it’s publicly accessible as a web server.

run is the command to create a new container

The --name flag is how you specify the name of the container. If left blank, a generated name like nostalgic_hopper will be assigned.

-p specifies the port you are exposing in the format of -p local-machine-port:internal-container-port. In this case, you are mapping port :80 in the container to port :80 on the server.

nginx is the name of the image on Docker Hub.

now this will show this on your public ip

## In your terminal, enter CTRL+C to stop the container from running.

```bash
docker ps -a
```

## verify the container status with this command

```bash
docker rm docker-nginx
```

## Remove the existing container

```bash
docker run --name docker-nginx -p 80:80 -d nginx
```

## Create a new, detached Nginx container,By attaching the -d flag, you are running this container in the background.

```bash
docker ps
```
## this will obtain info about your container

```bash
docker stop docker-nginx
```

## Stop the container

```bash
docker rm docker-nginx
```

## remove the container

# Building a Web Page to Serve on Nginx

```bash
mkdir -p ~/docker-nginx/html
```

## Create a new directory for your website content within the home directory

```bash
cd ~/docker-nginx/html
```

## by this you navigate into this

```bash
vi index.html
```

## now press i and write your code in html like 


![Screenshot_2024_0923_211405](https://github.com/user-attachments/assets/7cd1afd2-b42e-43c1-94ed-86a1f1ebedf9)

## then press ctrl+c then shift+colon then write wq and enter

```bash
docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx
```

Linking the Container to the Local Filesystem

## open your public ip in browser you will see as the content as your html code


# Using Your Own Nginx Configuration File

```bash
cd ~/docker-nginx
```


```bash
docker cp docker-nginx:/etc/nginx/conf.d/default.conf default.conf
```

## Copy the Nginx config directory into your project folder

```bash
docker stop docker-nginx
```

```bash
docker rm docker-nginx
```

## to rebuild the container stop the container then remove it

```bash
docker run --name docker-nginx -p 80:80 -v ~/docker-nginx/html:/usr/share/nginx/html -v ~/docker-nginx/default.conf:/etc/nginx/conf.d/default.conf -d nginx
```

## This command links the custom website pages to the container.

```bash
docker restart docker-nginx
```

## you need to restart your container to reflect changes on the associated pages.


# Kubernestes :- 

Kubernetes (sometimes shortened to K8s with the 8 standing for the number of letters between the “K” and the “s”) is an open source system to deploy, scale, and manage containerized applications anywhere.

Kubernetes has built-in commands to handle a lot of the heavy lifting that goes into application management, allowing you to automate day-to-day operations. You can make sure applications are always running the way you intended them to run.

![Screenshot_2024_0923_215514](https://k21academy.com/wp-content/uploads/2020/06/Kubernetes_Architecture-1.png)

# Minikube:-

Minikube is a tool that sets up a Kubernetes environment on a local PC or laptop. This tool  provides an easy means of creating a local Kubernetes environment on any Linux, Mac, or Windows system, where you can experiment with and test Kubernetes deployments.

![Screenshot_2024_0923_215611](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg)


# USING MINIKUBE IN AWS

##First open aws search EC2 ,and download your passkey then Launch Instance and select 22.04 AMI then select t2.xlarge instance type then select keypair then configure storage to 30 GB then enable all traffic in network and Launch.

##Launch PuTTY and add the IP address from instance and add key pair file and open the PuTTY terminal.

## Now connect it with putty and login into it by writing ubuntu

## Now put some commands


```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

## it will install docker


```bash
sudo usermod -aG docker $USER
```

```bash
newgrp docker
```

## it will Add your local user to docker group so that your local user run docker commands


```bash
sudo snap install kubectl --classic
```

## it will intall kubernetes


```bash
kubectl version --client
```

## it checks the version

# Installing Minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```


```bash
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

```bash
minikube version
```

## it checks its version

## Starting Minikube with Docker Driver

```bash
minikube start --driver=docker
```

# If you encounter root privileges error, run:


```bash
minikube start --driver=docker --force
```

```bash
minikube status
```

## it checks its status


```bash
kubectl cluster-info
```

## it checks cluster info


```bash
kubectl config view
```

## it will show the config


```bash
kubectl get nodes
```

## it will display nodes in it

```bash
kubectl get pods
```

## it will show pods in it

```bash
kubectl create deployment nginx-web --image=nginx
```

```bash
kubectl expose deployment nginx-web --type NodePort --port=80
```
kubectl get deployment,pod,svc

## it will deploy a sample nginx deployment


```bash
minikube addons list
```


```bash
It will display all addons
```


```bash
minikube addons enable dashboard
```

```bash
minikube addons enable ingress
```

## this enables these addons

```bash
minikube dashboard --url**
```

# it will get the url and run the dashboard of MiniKube


```bash
kubectl proxy --address='0.0.0.0' --disable-filter=true &
```


## This will enable port :8001 to access it on your public ip


```bash
http://server_ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=default
```

# in browser replace server ip with public ip

# Now go to above link and replace server_ip with your public ip and it will show you like :

![Screenshot_2024_0923_213426](https://github.com/user-attachments/assets/16ca5aa7-e6db-47d4-b005-2794b6c4289b)


# Openstack :-

OpenStack is an open-source platform that enables the creation and management of cloud computing services. It provides a web interface for controlling computing power, storage, and networking resources in a data center. This allows organizations to build their own private or public clouds, simplifying the deployment and management of applications.

![Screenshot_2024_1104_185043](https://object-storage-ca-ymq-1.vexxhost.net/swift/v1/6e4619c416ff4bd19e1c087f27a43eea/www-assets-prod/openstack-map/openstack-map-v20240401.png)


# VPC

Amazon Virtual Private Cloud (VPC) is a virtual network that allows users to launch AWS resources in a logically isolated environment. It's a foundational service of AWS that gives users complete control over their virtual networking environment. 

### What is the difference between EC2 and VPC?

•EC2 is a virtual server that you can run your software on. VPC is a virtual network that you use to connect your virtual servers, and other resources.

### Go to VPC and create a VPC then we  have to create 4 subnets , where 2     subnets are private and other two are  public .

![Screenshot 2024-11-06 130744](https://github.com/user-attachments/assets/69c1c2c7-7b44-4fc5-9d73-d36aa78a7935)


![Screenshot 2024-11-06 125448](https://github.com/user-attachments/assets/40f24cd8-b8af-4f59-8530-f6a60efbe3f7)



## gateways:- 

 INTERNET GATWAY , whic is  to be connected to your VPC which is   created earliy.

![Screenshot 2024-11-06 125549](https://github.com/user-attachments/assets/f08b24c2-cc4e-49b1-9e7f-9d2390ed214a)


## route tables 


![Screenshot 2024-11-06 130136](https://github.com/user-attachments/assets/87a743ab-0484-476f-bc44-1b6efa546b94)


##  load  balanceR

![image](https://github.com/user-attachments/assets/2bb320a8-a678-4140-9a30-817bebcd54a4)



*now put on any one instance write following commands in putty -*

* ```
  htop
  ```
  ```
  seq 999999999999999999999999999999999999999999999999999999999 > /dev/null &
  ```
  ```
  htop
  ```

  ![Screenshot_2024_1104_183758](https://github.com/user-attachments/assets/bae13bf3-7e99-4944-86fb-156efc303382)

# NETWORKING 

### types of network 

![Screenshot_2024_1105_071234](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEirLeSagDIvqf5VQpAIankKXm3uMvUPceToM722xg6sE8bK7wcL8aU6nnhIht_LG6p5SMy_GkpfTbsnmrfmAR5d52B4Pj8-HrrxzXOuPyWdMe3PR2DyN6bCix7aFZ-uOTFKvZFpcj2GDKI/s1600/Types+of+Computer+Networks+%28www.tutorialsmate.com%29.png)


## Network Devices:-

### 1. network adaptor/ interface 
   
   • connects a device to network. 
   
   • has a Mac address by manufacturer 
   
   • second layer device 

### 2. switch 
   •it is a very multiport network         bridge that uses MAC address to        forward data
   
   •link layer device 

### 3. Router 
   •it is a device that forwards          data between computer networks
 
   • 3rd layer device 

### 4. HUB 
   •network device that used to            connect multiple computers in a        network 
 
   • all information send to the hub       is automatically send to each port     to every device 

### 5. TAP
  (WORKS ON LAYER 2 -- ethernet frame )

used to create a user space network bridge.

### 6. TUN 
 ( WORKS ON LAYER 3 -- IP packets )

 create a tunnel network to reach       another network .
   

## 7. OVS :- Open virtual switch 

it is used with hypervisors to interconnect virtual machines within a host and between different hosts accross networks.

## 8. QEMU :- Quick emulator 
## Basic terms for understanding networking better:- 

## 1.NAT :- 

it is a process in which one or more local IP addresses are translated into one or more global IP addresses and vice versa

## 2. veth :-

these are pair of virtual network interfaces that are used to connect network namespaces together.

## 3.DPDK :- Data Plane Development Kit

it is a set of libraries and drivers that accelerates packet processing and their ability to create packet forwarders without the need of costly custom switches and routers

 ## 4. NIC :- network interface card 

 It allows one device to connect to     network

 ## 5. DPU :- Data Processing Unit 

 it is a new programmable processor that helps move data around data centres. it ensures right data goes to right place in right format quickly .

## 6.CSI :- Container Storage Interface 

free open source machine it can run various guest operating systems (OS's ) and architecture on a single host system.

## 9. Docker :- 

it is like a container that holds everything your application needs to run including the code, libraries.


## 10. Kubernets :- 

it is like a manager for containers .it helps to deploy, scale and manage a group of containers making sure they run smoothly.


## 11. web assembly:- (WASM)

technology that allows you to run code written in different programming languages. It is a way to build high speed, responsive web applications that can handle data and communicate over networks.

## 12. Firewall :- 
security system that controls incoming and outgoing network traffic based on pre- determined security rules.

## 13. DMZ :- 
 
![Screenshot_2024_1105_054347](https://github.com/user-attachments/assets/bd343550-a15b-485c-a9c5-46ec430901b3)


## 14.  VxLAN :- 
It is tunneling report that tunnel Ethernet traffic (layer 2) over an IP network(layer 3).

  ### 14.1 VTEP:- 
   it is a device that's responsible      for encapsulating and de-capsulating
   layer 2 traffic.

## 15. LINUX Bridge :- 

it is a kernel module that behaves like a network switch .It is usually used for forwarding packages on routes or gateways or between virtual machines.

## 16. Pktgen :- 
it is a tool for high speed package generation and testing. It  in the Linux kernel.

### netns :- network namespace 
 feature of Linux kernel that provides a way to create isolated network environment.

***TAP is often used to connect VM or containers to a physical network***

## KVM :- kernel virtual machine 
( typer 1 hypervisor)


## CNI :- Container Networking Bridge 

it is responsible for setting up the network ( assigning IP address, create network bridge) for containers ,enabling communication between containers and outside world

***examples***
VLAN , IPvLAN , CALICO , FLANNEL , VMware. etc 

### Flannel :- 
it acts as a layer that allows containers to send and receive data seamlessly accross various hosts .
 
  ### working:- 
  it runs a small single binary agent    on every host.
  this networking tool gives every       host an IP subnet.

  

## Packet Switching:- 

when we send email or web page the data does not travel as single continuous stream instead is broken down into smaller chunks called packets .


## key functions of network core :-

## 1. Forwarding :- 
  
• it is a local action of moving and     arriving packets from a router's       input to appropriate router output     link.


## 2. Routing :- 
 • global process of determining the      full paths packets take from source    to destination


## Network Protocols:- 
set of rules that determine how the packet is to be transferred and received and in which format .


### 1. TCP 
 
  it ensures reliable order delivery of data between applications . It handles things like breaking data into packets

### 2. IP 

 responsible for addressing and routing packets across the internet. 

 
### 3. HTTP 

 it is a protocol that powers the world wide web defining how messages are formatted and transmitted between web browsers and servers.





