# Rolax Resort

A dummy site used for training.

## steps to build the docker image for local testing

docker run -d -p 80:80 html-server-image:v1
 docker images
REPOSITORY           TAG       IMAGE ID       CREATED          SIZE
rolax-resort-image   v1        16a177961c9b   21 seconds ago   51.7MB
kindest/node         <none>    32b8b755dee8   21 months ago    1.12GB

% docker run -d -p 80:80 rolax-resort-image:v1
2bfbc3d3bd1193987028c72c447329978c07cdb4d075ec5aede52ab6daa84a09

Access the link using http://localhost


Logged in to Azure Portal

Created a Resource Group
Created Container Registry

Cli Login for docker :

docker login rolaxresort.azurecr.io --username 44dacde6-8608-413c-a507-73a91aa45940 --password $TOKEN

az acr build --image rolax-resort-image:v1 \
  --registry rolaxresortscr.azurecr.io \
  --file Dockerfile .



  Container instance Public I : http://4.158.10.123/



  Creating Azure AKS: 
  we need to link the container registry, and here I get error as:
  You must be a subscription contributor with the user access administrator role or a subscription owner in order to connect Azure Container Registry with Azure Kubernetes Service.

  AKS Cluster is not possible with this account

  # List all deployments in a specific namespace
# Format :kubectl get deployments --namespace <namespace-name>
kubectl get deployments --namespace kube-system