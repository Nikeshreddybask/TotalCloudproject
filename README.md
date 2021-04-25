# TotalCloudproject

## Assignment for kubernetes application - TODO Application
- To build the docker image for demo code use below commands

- Language: Node.js
- Pre-req: Kubernetes cluster
- cli tools required: docker, kubectl, git

Step 1: Perform the git clone and check out the code

Step 2: Build the docker images
```zsh
docker build -t demo .
```
Step 3: Docker image will be created
```zsh
docker images
```

Step 4: Deploy application in docker
```zsh
docker run -dp 3000:3000 demo
```

Step 5: Tag the docker image and push to docker hub
```zsh
docker tag demo nikdoocker2293/demo:v1
docker login
docker push nikdoocker2293/demo:v1
```

Step 6: Deploy the application in kubernetes cluster
```zsh
// Deployment.yaml file creates a deployment and pod object.
kubectl create -f deployment.yaml
// svc.yaml expose the above deployment through Type: LoadBalancer
kubectl create -f svc.yaml



