# vthwin-os

A full-stack personal platform and job command center engineered out of a single decoupled repository. This project serves a public professional portfolio that's designed around a GitOps continuous delivery lifecycle.

### 🏗️ Architectural Overview

- **Frontend UI:** A decoupled, single-page client dashboard built with **React, TypeScript, and Material UI**.
- **Headless API:** A high-throughput backend service engineered using **Spring Boot 3.x** and **Java 25**.
- **Data Layer:** A flexible, polymorphic document schema hosted on **MongoDB Atlas** that manages real-time application pipelines, state-machine tracking statuses, and dynamic portfolio content variations.

### 🚀 GitOps & Infrastructure Lifecycle

This system transitions away from traditional imperative deployments to a fully declarative GitOps pipeline.

1. **Continuous Integration:** GitHub Actions orchestrates automated Maven and Node test suites, compiles multi-stage production **Docker** containers, and pushes unique image tags to the container registry.
2. **Continuous Delivery:** An **ArgoCD** engine tracks the `infrastructure/` directory on the `main` branch, monitoring declarative Kubernetes manifests (`Deployments`, `Services`, `Secrets`) and executing zero-downtime rolling updates to keep the live single-node cluster perfectly synchronized with Git.
3. **Resource Optimization:** Configured with strict JVM memory boundaries (`-Xms128m -Xmx256m`) and Serial Garbage Collection (`-XX:+UseSerialGC`) to run smoothly on a minimal, low-cost enterprise footprint.
