📦Voting Application on Kubernetes (Docker Desktop)
🚀 Project Overview

This project demonstrates deploying a microservices-based voting application on a Kubernetes cluster enabled via Docker Desktop.
It showcases container orchestration, service communication, and traffic routing using Kubernetes..

🏗️ Architecture
User → Ingress → Service → Vote App
                         ↓
                       Redis
                         ↓
                       Worker
                         ↓
                    PostgreSQL
                         ↓
                Result Service → Result App
                
Sourece Code: https://github.com/mohammedashiqu/docker-voting-app-new

🧰 Tech Stack
Docker Desktop (Kubernetes Cluster)
Kubernetes (Deployments, Services, Ingress)
Docker (Containerization)
Python, Node.js, .NET
Redis (Queue)
PostgreSQL (Database)
⚙️ Prerequisites
Install Docker Desktop
Enable Kubernetes in Docker Desktop settings
Install kubectl
🚀 Deployment Steps
1. Clone repository

2. Apply Kubernetes manifests
kubectl apply -f k8s/

3. Verify pods
kubectl get pods

4. Verify services
kubectl get svc

5. Verify ingress
kubectl get ingress


🌐 Access Application
If using Ingress:
Add entry in hosts file:
127.0.0.1 voting-app.local
Access:
http://voting-app.local
If using NodePort:
http://localhost:<nodeport>


🔄 Application Workflow
User submits vote via frontend
Vote stored in Redis
Worker processes vote
Data saved in PostgreSQL
Results displayed in UI


🔍 Troubleshooting
kubectl logs <pod-name>.
kubectl describe pod <pod-name>.
kubectl get all.


📈 Features
1. Microservices architecture.
2. Kubernetes-based deployment.
3. Self-healing and scaling.
4. Internal & external service communication.


🧠 Learnings
1. Kubernetes Deployments, Services, Ingress
2. Pod networking and service discovery
3. Debugging Kubernetes workloads
