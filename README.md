# nc42 project manifesto

The purpose of this document is to explain the goals and funding principles of the nc42 project.
As this document grows, sections may be splitted into sub directories, referencing those sections by hyperlinks.
This very file is the root of the directory.

## What is it and why does it exist ?

The purpose of the nc42 project is to create, and automate, open source tools, to deploy self-hosted cloud services.
Cloud providers like AWS or GCP are at the top of the inovation right now. A lot of people in the industry want to use their services, because, they are simply good.
However, there are some problems with those services:

+ They are entirely proprietary, no source code is available. (The exception these days would be Microsoft who is releasing some Azure components code, but this is a slow process and it is unlikely we could see one of those platforms releasing their entire code)
+ The data you put on those platforms is not safe. More important, some governemental organization could access it, without you any notice. This is also true, for the organizations of foreign countries. You can indeed, choose the region where you want to put your workloads, but guess where all the backups go ?
+ Once you deploy your production infrastructure on one of those platforms, you are dependant. Initiatives and technologies exist to enable you to balance your deployments between multiple cloud provider (multi-cloud), to deploy your services anywhere else almost the same way (infrastructure as code), or simply backup all your data, code and configurations plus provide a fail-over. Those techniques do exist, but are not easy to implement and do have drawbacks as it is always painful to replace the underlying infrastructure of a company production.
+ They can be expensive. Those platforms are great, to either start a project, or innovate and add new features to an existing project, they are really evolutive and simple to use. However this has a cost and the longer your project will rely on them, the most you'll realize it. If your workloads are heavy plus they don't evolve very fast, those platforms will be really expensive to use.
+ They encourage centralization of the Internet. A lot of companies and services on the Internet, rely on those platforms. This is questionnable in terms of resiliency (each time AWS is impacted by an incident, everyone notices it, as most of our daily usage services rely on it) and governancy.

### What is the difference with OpenStack, CloudStack, Kubernetes and other, open source, cloud related softwares ?

A huge one. nc42 is not about developing a IaaS software, or a container orchestrator.
It is about linking great projects (like those ones) together, picking parts of them and creating automation above them, in order to provide an easy to use, modular project. The idea is to permit to deploy a complete, resilient and scalable, self hosted, infrastructure, that provides efficient and reliable cloud services.
The way that project has to be architectured, aims to permit to deploy either a full architecture, one, or more parts of it, depending on your needs.

## Project Guidelines

This project is guided by the following principles:

+ **Infrastructure As Code**: we aim to create idempotent, self explanatory, reliable code, which main goal is to deploy infrastructure.
+ **Community**: we don't want you, to blindly use our tools. We aim to provide tools that permit to get infrastructure management easier and faster, but in an understandable way. Our goal is to write good quality documentation and make you wish to get involved.
+ **KISS and UNIX phylosophy**: we will strive to guide our choices to deliver tools as simple as possible, following the Keep It Simple and Stupid principle. Those tools should also do one thing (or at least, not more than a few things) and do it well, following the well known principle from the UNIX world.
+ **Security**: we aim to deliver tools as secure as possible, staying tuned on security best practices (https://bettercrypto.org/ for example) and keeping our code and tools up to date.
+ **(Horizontal) Scalability**: the tools we build have to be designed with scalability in mind. Anyone should be able, using them, to deploy the same features on either one, ten or a thousand servers (physical or virtual depending on the services you want). We surely couldn't afford huge infrastructures to test it by our selves, but here's where the collaboration in the community is important.
**Efficiency**: the footprint of those tools, has to be as low as possible. Deployments also have to be as fast as possible. We aim to provide performances tests in our release process.
