# Voting App

A simple distributed application running across multiple Docker containers.

This app uses Python, Node.js, .NET, with Redis for messaging and Postgres for storage.

The folder k8s-specifications contains the YAML specifications of the Voting App's services.

The `vote` web app is then available on port 31000 on each host of the cluster, the `result` web app is available on port 31001.

## Architecture

![Architecture diagram](architecture.excalidraw.png)

* A front-end web app in [Python](/vote) which lets you vote between two options
* A [Redis](https://hub.docker.com/_/redis/) which collects new votes
* A [.NET](/worker/) worker which consumes votes and stores them in…
* A [Postgres](https://hub.docker.com/_/postgres/) database backed by a Docker volume
* A [Node.js](/result) web app which shows the results of the voting in real time

## WorkSnapShots

![1](https://github.com/dengineer2104/voting-app/blob/main/Resources.png)
![2](https://github.com/dengineer2104/voting-app/blob/main/ACR.png)
![3](https://github.com/dengineer2104/voting-app/blob/main/AllPipleines.png)
![4](https://github.com/dengineer2104/voting-app/blob/main/Pipeline.png)
![4](https://github.com/dengineer2104/voting-app/blob/main/SVC.jpg)
![6](https://github.com/dengineer2104/voting-app/blob/main/ArgoSettings.png)
![7](https://github.com/dengineer2104/voting-app/blob/main/Argo.png)
