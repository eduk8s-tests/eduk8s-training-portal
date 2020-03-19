Training Portal
===============

This repository contains sample configuration for demonstrating the eduk8s
training portal.

Prerequisites
-------------

In order to use the workshop you should have the eduk8s operator installed.

For installation instructions for the eduk8s operator see:

* https://github.com/eduk8s/eduk8s-operator

Specific workshops may have their own requirements. The workshops currently
being used are:

* https://github.com/eduk8s-labs/lab-k8s-fundamentals
* https://github.com/eduk8s-labs/lab-octant-testing

Check each for any further requirements, such as installation of other
operators, availability of certain persistent volumes types etc.

Deployment
----------

To deploy the sample training portal configuration run:

```
kubectl apply -k github.com/eduk8s-tests/eduk8s-training-portal
```

Then run:

```
kubectl get trainingportal/eduk8s-training-portal
```

This will output the URL to access the web portal for the training environment.

You need to be a cluster admin to create the deployment using this method.

Deletion
--------

To delete the training portal deployment, run:

```
kubectl delete -k github.com/eduk8s-tests/eduk8s-training-portal
```
