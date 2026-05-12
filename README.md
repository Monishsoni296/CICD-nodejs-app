# Serverless Node.js CI/CD Pipeline 🚀

A fully automated, cloud-native CI/CD pipeline for a Node.js API, demonstrating containerization of an application and deploying it to a serverless environment with automated scaling.

---

## 🔗 Live Application
**API Endpoint:** [View Live API](https://node-app-serverless.lemonglacier-4fe517bd.eastus.azurecontainerapps.io/api/videos)  
*(Note: If the link takes a few seconds to load, it is because the serverless environment is "Scaling up" from zero.)*

---

## ✨ Project Highlights
- **Zero-Downtime Deployment:** Uses GitHub Actions to push updates without manual intervention.
- **Dockerized Architecture:** Ensures the app runs identically in development and production.
- **Serverless Hosting:** Hosted on **Azure Container Apps**, configured to "Scale to Zero" when idle to eliminate unnecessary cloud costs.
- **Secure Secrets Management:** All credentials (Azure, Docker Hub) are managed securely via GitHub Encrypted Secrets.

---

## 🛠 Tech Stack
- **Backend:** Node.js, Express.js
- **Containerization:** Docker
- **Registry:** Docker Hub
- **CI/CD:** GitHub Actions
- **Cloud Provider:** Microsoft Azure (Container Apps, Managed Environments)

---

## 🏗 Pipeline Workflow
1. **Push:** Code is pushed to the `main` branch.
2. **Build:** GitHub Actions triggers a build job using a `Dockerfile`.
3. **Registry:** The image is tagged and pushed to **Docker Hub** (`monishsoni20/nodejs-cicd-app`).
4. **Deploy:** GitHub Actions authenticates with Azure using a Service Principal and triggers a deployment to the **Azure Container App Environment**.
5. **Serve:** Azure pulls the latest image and serves the API on port 3000.
