# Kubectl Command Reference
#### 1. Knowing kubectl version
``` sh
$ kubectl version
```
> Gives information about the version of kubectl installed on the system
```
Output:
Client Version: version.Info{Major:"1", Minor:"20", GitVersion:"v1.20.1", GitCommit:"c4d752765b3bbac2237bf87cf0b1c2e307844666", GitTreeState:"clean", BuildDate:"2020-12-19T08:38:20Z", GoVersion:"go1.15.5", Compiler:"gc", Platform:"darwin/amd64"}

Server Version: version.Info{Major:"1", Minor:"20", GitVersion:"v1.20.0", GitCommit:"af46c47ce925f4c4ad5cc8d1fca46c7b77d13b38", GitTreeState:"clean", BuildDate:"2020-12-08T17:51:19Z", GoVersion:"go1.15.5", Compiler:"gc", Platform:"linux/amd64"}
```
#### 2. Get nodes in a cluster
```sh
$ kubectl get nodes
```
> Gives information about the number of nodes in the cluster
```
Output:
NAME       STATUS   ROLES                  AGE   VERSION
minikube   Ready    control-plane,master   8h    v1.20.0
```
#### 3. Deploy POD in a cluster
```sh
$ kubectl run nginx --image nginx
```
> Downloads the docker image nginx from dockerhub
> and deploys docker container image on the pod nginx
```
Output:
pod/nginx created
```
#### 4. Get PODs in a cluster
```sh
$ kubectl get pods 
```
> Gives information about the number of pods deployed in the cluster
```
Output:
NAME    READY   STATUS    RESTARTS   AGE
nginx   1/1     Running   0          38m
```
#### 5. Describe POD with kubectl 
```sh
kubectl describe pod nginx
```
