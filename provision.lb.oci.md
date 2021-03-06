# How to Provision OCI Load Balancer for Oracle WebLogic Cluster

## Pre-requisite

This guide assumes you have already provisioned separate subnet with its appropriate security lists that allow communication between lb_subnet and WebLogic subnet. It is essential to use **separate subnet.**

## Provision OCI Load Balancer

Now login to your Oracle cloud tenancy from http://cloud.oracle.com with your tenancy ID, username and password.  

Click on the Menu on the top left hand corner and select 'Networking' -> 'Load Balancers'. Then click Create Load Balancers: 

![cluster1](images/weblogic_install/lb1.jpg)  

Insert the desired load balancer name, choose it as public then choose the bandwidth. Choose the correct VCN and subnet for load balancer like below and click next:  

![cluster2](images/weblogic_install/lb2.jpg)  

Choose Weighted Round Robin then add backends, in this case choose 2 VM that hosting WebLogic cluster:

![cluster3](images/weblogic_install/lb3.jpg)

After that change the port to 7003 as that port is used for the application, and also put 7003 into health check port, click next:

![cluster4](images/weblogic_install/lb4.jpg)  

Input the desired load balancer listener name, and choose HTTP and click submit like below:  

![cluster5](images/weblogic_install/lb5.jpg)  

After we wait for some time then we will see this console, we take the IP Public address, wait some time to test in the browser:  

![cluster6](images/weblogic_install/lb6.jpg)  
