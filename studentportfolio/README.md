# COMP-4001: Module 6 - Assignment Part 3
## Student Profile: Neil Tolentino
- **Student ID:** 0392308
- **Program:** Full-Stack Development - RRC Polytech

## Project Overview: GitOps CI/CD Pipeline
This project demonstrates a fully automated, production-ready GitOps pipeline for 
the Pixel River Financial Bank Application. It transitions the previous manual and 
scripted deployments into a modern, observable loop where code changes trigger 
automated builds and deployments.

### Key Technical Components:
* **Continuous Integration (CI):** Handled by GitHub Actions. Upon code push, it 
builds unique Docker images tagged with the GitHub SHA and pushes them to the 
GitHub Container Registry (GHCR).

* **Deployment Artifact Generation:** 
The pipeline automatically updates the Kubernetes manifests in the GitOps 
repository to reflect the newest image tags.

* **Continuous Delivery (CD):** Managed by Argo CD. It monitors the "Single 
Source of Truth" in Git and synchronizes the cluster state automatically, 
ensuring the live environment matches the desired configuration.

* **High Availability:** The backend and transaction services are deployed with 
multiple replicas and managed by Horizontal Pod Autoscalers (HPA).

## Student Portfolio Branding
In accordance with the rapid development requirements, the index.html and 
login.html files have been modified to reflect my professional profile and the 
specific branding for the Pixel River Financial Bank Application.

## Repository Structure
* **Source Repository:** Contains the microservice source code and GitHub Actions workflows.
* **GitOps Repository:** A private repository containing the declarative Kubernetes manifests used by Argo CD.