# Clustering

## What is a Computer Cluster? 
A computer cluster consists of multiple racks that consists of computers. There are no peripheral devices (keyboard/mice), meaning no direct Shell access to these devices. However, all of these are connected through a top node/host computer that is connected to the internet.

<img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimages.wisegeek.com%2Froom-full-of-computer-servers.jpg&f=1&nofb=1" alt="System Cluster" height="200">

These computers can be called, nodes, hosts or just computers and are usually denoted with names that move up in order such as ma001.. ma002 and forward  
All of these computers are connected together through ethernet or a similar connection

The head node/login node is the only one that is connected to the internet. There can be many head nodes but what is important is that there are a lot more ‘worker’ nodes that are not connected to the internet.

Additionally, there are storage clusters that are used with network storage or storage arrays. These are a shared resource including the computer cluster. 

Each node on the cluster has a purpose and trying to complete all tasks on one head node would most likely result in a crash. 

First you would login into the head node to access our storage array, then when we would like to perform an operation we move to one of our other working cluster nodes. This worker/compute node will access the same information from the storage arrays. Therefore, where our calculations come from in this cluster does not matter. It will all be duplicate information. 

---

## Where do we run code or run our programs? 

<img src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fmedia.gettyimages.com%2Fvideos%2Fhigh-school-teacher-handing-out-assignment-papers-video-id103453686%3Fs%3D640x640&f=1&nofb=1" alt="Teacher Hands out HW" height="200">

If we have only two or three people we can just say, “Hey Bill, I’m using ma001, ma002 and ma003 today.” Then you would just use ma004… and so on. However, what do we do when we have many others?


We then use something called Dynamic Resource Manager (Scheduler) and make a job script saying what we want done. The name of the program, where to find input and where to place the output. This is submitted to the scheduler and decides where to run this code. It will choose an open worker to use and schedules them so there are no conflicts. 


Once done, output will be placed where you specified. You can then collect your information through the head node once your program has run through the DRM/Scheduler.

---
