# DataZip Internship Assignment: Superset with Kubernetes Setup

## Setup Instructions

1. **Install Minikube**
   Follow the official Minikube installation guide for your operating system:
   https://minikube.sigs.k8s.io/docs/start/

2. **Install Kubernetes**
   Kubernetes comes pre-installed with Minikube. No additional installation is required.

3. **Install Docker**
   Follow the official Docker installation guide for your operating system:
   https://docs.docker.com/get-docker/

4. **Start Minikube**
   Open a terminal and run:

   ```
   minikube start --driver=docker

   ```
5. **Apply Kubernetes Configuration Files**
Apply all four YAML configuration files using:

    ```
    kubectl apply -f <file-name>.yaml
    ```
Repeat this command for each YAML file.

6. **Check Pod Status**
Verify all pods are running:
    ```
    kubectl get pods
    ```
7. **Check Services**
List all services:
    ```
    kubectl get services
    ```
8. **Access Superset URL**
Obtain the Superset service URL:
    ```
    minikube service superset
    ```
9. **Login to Superset**
Open the URL provided in step 8 in your web browser and log in to Superset.

10. **Add ClickHouse Database**
 - Navigate to `Data` > `Databases` > `+ Database`
 - Select "ClickHouse" from the database list

11. **Configure ClickHouse Connection**
 Fill in the following details:
 - Host
 - Port
 - Database name
 - Username

   
![Configure](/images/setup.jpg) 

12. **Establish Connection**
 Click the "Connect" button to establish the connection to ClickHouse.

![Deployed](/images/deploy.jpg)

