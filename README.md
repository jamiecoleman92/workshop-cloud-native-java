# Cloud-native Java Workshop

This workshop demonstrates the use of MicroProfile, Docker, Kubernetes and Istio technologies for implementing, deploy and update a set of cloud-native microservices. The workshop has be structured as 5 modules:
* **REST Foundation** covers the foundational technologies for producing and consuming REST services
* **Scalable Microservice Development** covers the technologies essential for developing and deploying microservices at scale where the microservices are the responsibility of autonomous teams.
* **Microservice Observability** covers the observability operational needs of microservice deployments at scale, such as tracing request and understanding microservice health.
* **Microservice Deployment and Update** covers the deployment, scaling and updating of microserivces at scale, through Kubernetes and Istio.
* **The Cloud** covers the deployment, scaling and updating of microserivces on the Cloud.

Each workshop module consists of a number of Open Liberty Guides each of which demonstrates a key cloud-native microservice technology. Each Guide is designed to be taken independently so if you just want to learn about a specific technology you can just take that guide. 

Please pick any guide you are interested in from the first part of the workshop and after the break we will do all the guides from the second part of the workshop. If you are finished and are feeling brave, try out the cloud section of the workshop. You can either try the IBM Cloud guide or OpenShift depending on what you prefer. Enjoy!!!

## Table of Contents

- [Cloud-native Java Workshop](#cloud-native-java-workshop)
  - [Table of Contents](#table-of-contents)
  - [Workshop Preparation](#workshop-preparation)
    - [Pre-requisites](#pre-requisites)
    - [Downloads](#downloads)
- [Introduction](#introduction)

### 1st Part of Workshop

- [REST Foundation](#module-1-rest-foundation)
    - [Creating a RESTful web service](#creating-a-restful-web-service)
    - [Injecting dependencies into microservices](#injecting-dependencies-into-microservices)
    - [Consuming RESTful services with template interfaces](#consuming-restful-services-with-template-interfaces)
- [Scalable Microservice Development](#module-2-scalable-microservice-development)
    - [Configuring Microservices](#configuring-microservices)
    - [Building fault-tolerant microservices with the @Fallback annotation](#building-fault-tolerant-microservices-with-the-fallback-annotation)
    - [Securing microservices with JSON Web Tokens](#securing-microservices-with-json-web-tokens)
    - [Documenting RESTful APIs](#documenting-restful-apis)
- [Microservice Observability](#module-3-microservice-observability)
    - [Providing metrics from a microservice](#providing-metrics-from-a-microservice)
    - [Adding health reports to microservices](#adding-health-reports-to-microservices)
    - [Enabling distributed tracing in microservices](#enabling-distributed-tracing-in-microservices)

### 2nd Part of Workshop
- [Microservice Deployment and Update](#module-4-microservice-deployment-and-update)
    - [Deploying microservices to Kubernetes](#deploying-microservices-to-kubernetes)
    - [Configuring microservices running in Kubernetes](#configuring-microservices-running-in-kubernetes)
    - [Checking the health of microservices on Kubernetes](#checking-the-health-of-microservices-on-kubernetes)
    - [Managing microservice traffic using Istio](#managing-microservice-traffic-using-istio)

### Extra Part of Workshop
- [The Cloud](#module-5-the-cloud)
    - [Deploying microservices to IBM Cloud]()
    - [Deploying microservices to OpenShift]()

## Workshop Preparation

To save time during the workshop, it's best to set up your machine beforehand. The instructions below show the pre-requisites to install and how to avoid lengthy downloads.

### Pre-requisites

To use these guides you need the following pre-requisites:
1. A Java 8 JDK (e.g. https://adoptopenjdk.net/?variant=openjdk8&jvmVariant=openj9)
2. Apache Maven 3.5.4 or later (https://maven.apache.org/). Older versions may not work.
3. A git client
4. An editor with Java support (e.g. Eclipse, VS Code, IntelliJ)
5. Docker & Kubernetes:
   1. Windows: https://docs.docker.com/docker-for-windows/#kubernetes 
   2. Mac: https://docs.docker.com/docker-for-windows/#kubernetes
   3. Linux: https://github.com/kubernetes/minikube#installation)
6. Download latest stable Istio release (not a Pre-release): https://github.com/istio/istio/releases

Below is only required for the extra part of the workshop (If you are feeling brave :D)

7. IBM CLI: https://cloud.ibm.com/docs/cli?topic=cloud-cli-install-ibmcloud-cli


# Introduction

Cloud-native is an approach to application development and deployment.  It's the product of a number of industry movements over the past 10-15 years - agile development practices, DevOps, Microservices and Cloud.  Cloud-native applications are developed using agile practices, use continuous integration/continuous delivery to streamline deployment, are architected around team-aligned microservices, and leverage the cloud for rapid deployment at scale.

When choosing which technologies to use for cloud-native microservices, the combination of open source and open standards can be very important.  The combination enables a low cost (free) of entry and at the same time avoids being locked in to a single vendor implementation.  

Eclipse MicroProfile is a set of industry specifications for developing and deploying cloud-native Java Microservices.  The specifications address the important challenges of cloud-native microservices, such as toleration of service failures, security, service metrics and health, and more.  Open Liberty is an open source, lightweight, composable Java server that implements the MicroProfile specifications.

Kubernetes is an Open Source platform for deployment, scaling and managing containers and services.  It uses a declarative yaml-based approach to describe deployments, for example, the containers to be deployed, their scaling requirements, the services they provide, and so on. 

Istio is an Open Source service mesh technology for the management of distributed microservices.  It enables securing, connecting and monitoring of microservice deployments.  Because Istio sits between the microservices in the mesh, it is able to route traffic (e.g. for blue-green deployments), handle faults (e.g. retry requests) and automatically secure service communications.

This workshop demonstrates how to address cloud-native microservice requirements using the combination of MicroProfile, Docker, Kubernetes and Istio technologies.  The workshop guides can be taken independently, or in the order they are introduced, below.

If you have feedback on a specific guide, we'd appreciated a github issue or pull request against that guide, and similarly if you have feedback on this workshop document, please raise an issue or submit a pull request. 

# Module 1: REST Foundation


### Creating a RESTful web service

Learn how to create a REST service with JAX-RS, JSON-P, and Open Liberty that will expose the JVM’s system properties.

The Guide: https://openliberty.io/guides/rest-intro.html

If you have feedback or find problems, please raise an issue here: https://github.com/OpenLiberty/guide-rest-intro


### Injecting dependencies into microservices    

Learn how to use Contexts and Dependency Injection to manage and inject dependencies into RESTful web services.      
        
The Guide: https://openliberty.io/guides/cdi-intro.html
       
If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-cdi-intro


### Consuming RESTful services with template interfaces    

Learn how to use MicroProfile Rest Client to invoke RESTful microservices over HTTP in a type-safe way.      
        
The Guide: https://openliberty.io/guides/microprofile-rest-client.html
       
If you have feedback or find problems, please raise an issue here:
https://github.com/openliberty/guide-microprofile-rest-client


# Module 2: Scalable Microservice Development

### Configuring Microservices

Learn how to inject external static and dynamic configuration to microservices using MicroProfile Config.

The Guide: https://openliberty.io/guides/microprofile-config.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-config


### Building fault-tolerant microservices with the @Fallback annotation

Learn how to use the MicroProfile Fault Tolerance specification to enable applications to function even when one
of the microservices is unavailable.

The Guide: https://openliberty.io/guides/microprofile-fallback.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-fallback
       

### Securing microservices with JSON Web Tokens

You’ll explore how to control user and role access to microservices with MicroProfile JSON Web Token (MicroProfile JWT).

The Guide: https://openliberty.io/guides/microprofile-jwt.html
        
If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-jwt


### Documenting RESTful APIs

Explore how to document and filter RESTful APIs from code or static files by using MicroProfile OpenAPI.

The Guide: https://openliberty.io/guides/microprofile-openapi.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-openapi


# Module 3: Microservice Observability


### Providing metrics from a microservice
 
Learn how to provide system and application metrics from a microservice using MicroProfile Metrics.

The Guide: https://openliberty.io/guides/microprofile-metrics.html
           
If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-metrics


### Adding health reports to microservices
   
Learn how to provide and check the health of a microservice using MicroProfile Health.

The Guide: https://openliberty.io/guides/microprofile-health.html
           
If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-health


### Enabling distributed tracing in microservices

Explore how to enable and customize tracing of JAX-RS and non-JAX-RS methods by using MicroProfile OpenTracing.

The Guide: https://openliberty.io/guides/microprofile-opentracing.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-microprofile-opentracing


# Module 4: Microservice Deployment and Update


### Deploying microservices to Kubernetes

Deploy microservices in Open Liberty Docker containers to Kubernetes and manage them with the Kubernetes CLI, kubectl.

https://openliberty.io/guides/kubernetes-intro.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-kubernetes-intro


### Configuring microservices running in Kubernetes

Explore how to externalize configuration using MicroProfile Config and configure your microservices using Kubernetes ConfigMaps and Secrets.

https://openliberty.io/guides/kubernetes-microprofile-config.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-kubernetes-microprofile-config


### Checking the health of microservices on Kubernetes

Learn how to check the health of microservices on Kubernetes by setting up readiness probes to inspect MicroProfile Health Check endpoints.

https://openliberty.io/guides/kubernetes-microprofile-health.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-kubernetes-microprofile-health


### Managing microservice traffic using Istio

Explore how to manage microservice traffic using Istio.

https://openliberty.io/guides/istio-intro.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-istio-intro


# Module 5: The Cloud

### Deploying microservices to IBM Cloud

Explore how to deploy microservices to IBM Cloud Kubernetes Service (IKS).

https://openliberty.io/guides/cloud-ibm.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-cloud-ibm

### Deploying microserives to OpenShift

Explore how to deploy microservices to Red Hat OpenShift.

https://openliberty.io/guides/cloud-openshift.html

If you have feedback or find problems, please raise an issue here:
https://github.com/OpenLiberty/guide-cloud-openshift
