# Deployment

Your deployment scenarios will vary WIDELY based on your company.  This module offers opinions and observations on some of them.

# Popular options for deploying distributed applications

## Kubernetes

By far [Kubernetes](kubernetes.io) is my favorite deployment option.

## Mesos/Marathon

[Mesos(http://mesos.apache.org )]/Marathon are a good choice if you have to deploy mixed workloads -- mixing Docker with non-docker workloads.  It requires a distributed file system to do this, so it's a much more complicated deployment.

## DCOS 

[DCOS](https://dcos.io) is free/commercial version of nicely packaged Mesos/marathon & more

Mesos/Marathon/DCOS notes- In production we had the hardest time with the Zookeeper requirement.  Zookeeper is hard to maintain and keep running without a lot of experience.

## Docker Swarm

Docker swarm is newer than any of the other orchestrators out there.  I've not used it, so can't give any practical advice.  Biggest complaint I hear is the lack of pluggability and extensibility in the model.

## CoreOS/Fleet

Fleet is a distributed task manager written for CoreOS.  Lighter than any of the other options, good if you like to roll your own.   

Bad if you're not using CoreOS.