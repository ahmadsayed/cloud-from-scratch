# Build Private Cloud From Scratch with Kubernetes.

Cloud used be defined in very simple way as follow  XaaS, X as a Service'
* IaaS Infrastructure as a Sevice
* PaaS Platform as a Service
* SaaS Software as a Service

## Ingredient 
* Few Baremetal machines.
* Few Networking device.
* Few Flash Disk.
* Few Master Minds in netwokring, storage and virtualization to assemble all of that together.

Lot of product the exists as commercial and Opensource to provide this capabilites such OpenStack, ApacheStack, vSphere, ... etc

So it is a matter of installing those tool and configuring it right ... !!! 
Unfortunatly those tools is either commercially very expensive, or come with its own challenge and learning curves and their own definition.

## What is a MVP Cloud Platform should Porvide.

One word the SDX family with the Rise of Cloud native more and more SDX come to play but what is SDX it Software Defined X
The major components are 
* SDN : Software Defined Networking
* SDS : Software Defined Storage

### SDN Software Defined Network
Controlling the traffic between your Virtual machines, is no longer configuration in your physical switch or router, with SDN we build some sort of Overlay accross all your physical host, and start rebuild the whole network and security policies around it.

### SDS Software Defined Storage
Providing a shared storage pool, is by bringing up All Flash appliance, or spinning Desks, Or SDS way of doing things is just bring Some machines and install SDS on top of them, so you will your Storage As A Service ready to serve ;).


## Kubernetes is more than just Container Orchestrator 


Kubernetes is the most used platform for container orchestration, a closer look at Kubernetes reveal that is is more than Just Container Orchestrator, as It provides the CXI where X is N or S 
* CNI : Container Network Interface 
* CSI : Container Storage Interface

### CNI and CSI in Kuberntes 
Which is an standard specs and libraries to be adopted by the industry and community to integrate Kubernetes with SDN such as NSX-T, Cisco ACI, Calico, .... .
Also CSI which give provide a standarized interface for Storage as well as Software Defined Storage.

### Custom Resource Definition
In Addition to standard Object, Kubernetes provide a good expandability with the custom resource definition make you able to create your own Resources the concepts extended by later with adopting the Operator Patterns.

### Kubevirt when Kubernetes meets LibVirt.
Let us put everything together, CNI, CSI , CRD, which can be used to define and create a compelete Virtual Machine not only Containers, or customized light weight VM, It is full blown VM and can be created, managed by Kubernetes as well as all Networking, Storage, provided by the Kubernetes API.

With that we have a compelete Solution that will provide the following IaaS (Virtual Machine, Storage, Networking), PaaS (Kubernetes Operators)

A single Unified API to manage the enviroments, Additionally the core functionalities Kubernetes itself of managing Containers, which will become more attactive when it managing the networking between containers and VM by the standard Kubernetes configurations.

## Without Further Ado let's build a Private Cloud 
