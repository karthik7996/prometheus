# EKS monitoring using prometheus

## clone the code to your cluster

* Create a Namespace monitoring **kubectl create namespace monitoring**

* Create the role using the following command **kubectl create -f clusterRole.yaml**

* Execute the following command to create the config map in **Kubernetes kubectl create -f config-map.yaml**

* Create a deployment on monitoring namespace using the above file **kubectl create -f prometheus-deployment.yaml**

* You can check the created deployment using the following command **kubectl get deployments --namespace=monitoring**

* First, get the Prometheus pod name **kubectl get pods --namespace=monitoring**

* Exposing Prometheus as a Service ( if you dont want to use port-forward ) **kubectl create -f prometheus-service.yaml --namespace=monitoring**
