Based on the candidate profile in the uploaded resume (DevOps Engineer with **4+ years experience in AWS, Azure, Kubernetes, Terraform, CI/CD, and DevSecOps**) , here is a **structured interview question set** including:

* Basic DevOps questions
* Advanced technical questions
* Scenario-based questions
* Tricky interviewer questions

These are suitable for **4–5 years DevOps Engineer interviews**.

---

# DevOps Interview Questions (4–5 Years Experience)

## 1. Basic DevOps Questions

1. What is DevOps and how is it different from traditional software development?
2. Explain the **CI/CD pipeline** and its stages.
3. What is **Infrastructure as Code (IaC)** and why is Terraform popular?
4. Difference between **Docker and Kubernetes**.
5. What is **Helm** and why do we use it?
6. Explain **blue-green deployment**.
7. Difference between **rolling deployment and canary deployment**.
8. What is **GitOps**?
9. What are **Kubernetes namespaces**?
10. What is the difference between **horizontal scaling and vertical scaling**?

---

# 2. AWS / Azure Cloud Questions

Since the candidate worked on **AWS EKS, VPC, RDS, Glue, Lambda** .

### AWS

1. Explain the architecture of **EKS**.
2. Difference between **EKS, ECS, and Kubernetes on EC2**.
3. What is **AWS Glue** and when would you use it?
4. What is the purpose of **AWS Step Functions**?
5. Difference between **SQS and SNS**.
6. How does **IAM role assumption work**?
7. What is a **VPC endpoint**?
8. How do you secure **EKS clusters**?

### Azure

1. What is **AKS architecture**?
2. Difference between **Azure Policy and Azure RBAC**.
3. What is **Azure Data Factory**?
4. What is **Azure Monitor**?

---

# 3. Kubernetes Interview Questions

1. Explain Kubernetes **architecture**.
2. Difference between:

| Component   | Purpose                  |
| ----------- | ------------------------ |
| Pod         | Smallest deployable unit |
| Deployment  | Manages pods             |
| ReplicaSet  | Ensures replica count    |
| StatefulSet | Stateful applications    |

3. What happens when a **pod crashes**?
4. Difference between **ClusterIP, NodePort, and LoadBalancer**.
5. How do you perform **rolling updates** in Kubernetes?
6. What is **ConfigMap vs Secret**?
7. How does **Kubernetes autoscaling work**?

---

# 4. Terraform Interview Questions

1. What are Terraform **modules**?
2. Difference between:

| Concept         | Meaning               |
| --------------- | --------------------- |
| Terraform State | Tracks infrastructure |
| Terraform Plan  | Preview changes       |
| Terraform Apply | Apply infrastructure  |

3. What is **remote backend**?
4. What happens if **Terraform state is lost**?
5. How do you manage **multiple environments (dev/prod)**?

---

# 5. CI/CD Pipeline Questions

Tools mentioned in resume: **Jenkins, GitHub Actions, ArgoCD, Azure DevOps** 

1. Difference between **CI and CD**.
2. What is **Pipeline as Code**?
3. Explain **GitHub Actions workflow**.
4. How do you secure **secrets in pipelines**?
5. What is **artifact management**?

---

# 6. Observability / Monitoring Questions

Resume mentions **CloudWatch, Azure Monitor, Dynatrace** .

1. What is **observability vs monitoring**?
2. How do you monitor **Kubernetes clusters**?
3. How does **CloudWatch alarm work**?
4. What metrics are important for **microservices monitoring**?

---

# 7. Scenario-Based DevOps Questions

### Scenario 1

Your **Kubernetes pods keep restarting in production**.

What will you check?

Expected answer:

* Pod logs
* Liveness/readiness probes
* Resource limits
* Node capacity
* CrashLoopBackOff

---

### Scenario 2

A **Terraform deployment failed midway** and some resources were created.

What will you do?

Expected approach:

* Check Terraform state
* Run `terraform plan`
* Import missing resources
* Fix state drift

---

### Scenario 3

Your **CI/CD pipeline suddenly takes 40 minutes instead of 10 minutes**.

What troubleshooting steps will you take?

Possible causes:

* Dependency download
* Docker build cache
* Slow artifact repository
* Infrastructure bottleneck

---

### Scenario 4

Your **EKS cluster nodes suddenly become NotReady**.

Possible checks:

* Node memory/CPU
* kubelet status
* networking (CNI plugin)
* IAM role permissions

---

### Scenario 5

Production deployment failed and users are impacted.

What is your rollback strategy?

Expected answer:

* Blue-green deployment
* Canary rollback
* Kubernetes rollout undo
* Artifact version rollback

---

# 8. Real DevOps Architecture Scenario

### Design Question

Design infrastructure for:

**Highly available microservices platform**

Requirements:

* Kubernetes
* CI/CD
* Monitoring
* Auto scaling

Expected architecture:

```
Developer
   |
GitHub
   |
CI/CD Pipeline (Jenkins/GitHub Actions)
   |
Docker Registry
   |
Kubernetes Cluster (EKS/AKS)
   |
Load Balancer
   |
Microservices Pods
   |
Monitoring (Prometheus / CloudWatch)
```

---

# 9. Tricky Interview Questions

These test **real experience**.

### Q1

What happens if **two engineers run Terraform apply simultaneously**?

Answer:
State corruption may occur → use **remote backend with locking (S3 + DynamoDB)**.

---

### Q2

Why should we **not store secrets in Kubernetes ConfigMap**?

Answer:
ConfigMap is **not encrypted** → use **Secrets**.

---

### Q3

If Kubernetes pod memory limit is exceeded, what happens?

Answer:
Container is **OOMKilled**.

---

### Q4

Why do Docker containers exit immediately?

Answer:
Main process finished.

---

### Q5

Why is Kubernetes not recommended for **stateful databases sometimes**?

Answer:
Storage, persistence complexity.

---

# 10. Behavioral DevOps Questions

1. Tell me about a **production outage you handled**.
2. How do you deal with **developer vs operations conflicts**?
3. How do you improve **deployment reliability**?
4. How do you implement **cost optimization in cloud**?

---

# Bonus: Rapid-Fire Questions

1. What is **sidecar container**?
2. What is **service mesh**?
3. What is **Helm chart**?
4. What is **GitOps workflow**?
5. Difference between **ArgoCD and Jenkins**?

---
