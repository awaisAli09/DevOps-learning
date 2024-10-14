# DevOps-learning
A written plan to learn devops tools and technologies.

1- learn a cloud platform - for now it would be AWS
2- Becoming proficient in infrastructure as code -- Terraform
3- Learning CI/CD - for now focus on Github Actions
4- learn Shell and python scripting
5- Docker and K8S

**More specific Plan:**

1-
- IAM
- EC2 - simply deploy a nodeJS application on EC2 and access it from outside
- learn about VPC, NACL and route53
- S3 - host a static website on S3
- Cloud Watch --> make EC2 CPU alerting through SNS
- AWS lambda
- deploy a 3 tier appication on aws


2-
 create a project by building and automating the infrastructure of a simple web application hosted on AWS. Start by setting up an **EC2 instance** with a web server (like Nginx), use **S3** for static file storage, and configure **IAM roles** and **security groups** for access control. Define all these resources in Terraform configuration files (.tf), ensuring they are modular for reuse. manage networking with **VPC**, and use **Elastic Load Balancer** for scaling. This will cover Terraform concepts like state management, variables, and resource provisioning.


3-
3.1. **Project Setup**:
 - get a simple Node.js/Next JS web application 
 - will include basic unit tests using a testing framework such as **Jest**.

3.2. **Create GitHub Actions Workflow**:
 - Create a `.github/workflows/ci.yml` file to define the workflow.
 - Add steps to:
 - **Checkout Code**: Use the `actions/checkout` action to pull your code.
 - **Install Dependencies**: Install your Node.js dependencies using `npm ci`.
 - **Run Tests**: Run your unit tests with `npm test`.
 - **Build the App**: Add steps to build the app, for example, `npm run build`.

3.3. **Deploy on Push to Main**:
 - Create another action in the same workflow or a separate one for deploying the app when code is merged into the `main` branch.
 - Use GitHub Actions to deploy to **AWS EC2**, by integrating with GitHub Actions.

3.4. **Notifications**:
 - Set up email notifications for build/test failures or successful deployments using GitHub Action plugins this will cover workflow triggers, job configurations, and deployment automation using GitHub Actions.

4-
- Create a project that focuses on building a Python script to monitor the health of servers in a DevOps environment. The script will periodically check key metrics like CPU usage, memory consumption, disk space, and network connectivity. It will log the results and send notifications via email if any metric exceeds defined thresholds.

5-
**Dockerize a Python Flask web application**. get a basic Flask app that serves a "Hello, Docker!" message, then write a `Dockerfile` that sets up the Python environment, installs dependencies, and runs the app. Build the Docker image and run it as a container, exposing the app on a local port (e.g., 5000). this will cover containerization, writing a `Dockerfile`, building images, and managing containers—all while working with a lightweight web app.
finally push your app image on Docker registry.

for K8S:
**deploy a simple Nginx web server** on a Kubernetes cluster. Start by writing a `Deployment` YAML file to define the Nginx app with replicas, then create a `Service` to expose the deployment externally. Use `kubectl` commands to apply the deployment and service to your cluster. This project will cover Pods, Deployments, Services, and interacting with the Kubernetes API, this will make grip on scaling and exposing applications.
