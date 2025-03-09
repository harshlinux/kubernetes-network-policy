#  Kubernetes Network Policy: Restricting Traffic to `my-app-deployment`

# Overview  
This repository contains Kubernetes manifests to deploy:
-  `my-app-deployment` (sample web application)
-  `cache-deployment` (caching service)
-  `my-app-service` (ClusterIP service exposing `my-app-deployment`)
-  `my-app-network-policy` (**NetworkPolicy** to restrict traffic)

# Network Policy Rules
-  **Allow incoming traffic** from **pods within the same namespace**.
-  **Allow incoming traffic** from pods **with label `app=trusted`**.
-  **Allow outgoing traffic** to **pods within the same namespace**.
-  **Deny all other incoming and outgoing traffic**.

---

##  Project Structure

---

##  Prerequisites  
Before deploying, ensure you have:
**Kubernetes cluster** (Minikube, Docker Desktop, or cloud-based K8s)  
**kubectl** installed and configured  
**CNI plugin (Calico)** to support Network Policies  
**Check if your cluster supports NetworkPolicies:**  
kubectl get pods -n kube-system
