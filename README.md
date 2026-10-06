# Hey 👋 I'm Muralidharan

### Software Engineer | Backend • Go • AWS

Software engineer who enjoys untangling ambiguous problems, building reliable backend systems, and learning whatever tools the problem demands.

Currently focused on:

- 🐹 Building backend systems with **Go**
- ☁️ Working with **AWS** and event-driven architectures
- 🧠 Strengthening **DSA & problem solving**
- 🤖 Exploring practical **AI + backend engineering**
- 🚀 Building software that is reliable beyond the happy path

---

## 🛠️ Core Stack

### Backend

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-02569B?style=flat-square)
![Gmail API](https://img.shields.io/badge/Gmail_API-EA4335?style=flat-square&logo=gmail&logoColor=white)

### AWS & Infrastructure

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![ECS](https://img.shields.io/badge/ECS_Fargate-FF9900?style=flat-square&logo=amazonecs&logoColor=white)
![SQS](https://img.shields.io/badge/SQS-FF9900?style=flat-square&logo=amazonsqs&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white)
![RDS](https://img.shields.io/badge/RDS-527FFF?style=flat-square&logo=amazonrds&logoColor=white)
![CloudFront](https://img.shields.io/badge/CloudFront-8C4FFF?style=flat-square&logo=amazonaws&logoColor=white)
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat-square&logo=amazonaws&logoColor=white)
![ECR](https://img.shields.io/badge/ECR-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-232F3E?style=flat-square&logo=amazonaws&logoColor=white)

### Development & CI/CD

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

# 🚀 Featured Project

## ApplyFlow

**Outreach that keeps going after you close the laptop.**

ApplyFlow is a job-application outreach system I built to automate personalized
email campaigns from a spreadsheet.

The system accepts a list of companies and roles, processes applications
asynchronously, and sends emails through Gmail without keeping the user
waiting for each individual operation.

### Architecture

```text
                         ┌──────────────────┐
                         │   React + Vite   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │     Go API       │
                         └──────┬─────┬─────┘
                                │     │
                     ┌──────────┘     └──────────┐
                     ▼                           ▼
              ┌─────────────┐             ┌─────────────┐
              │ PostgreSQL  │             │     S3      │
              └─────────────┘             └─────────────┘
                                                   
                                  │
                                  ▼
                         ┌──────────────────┐
                         │       SQS        │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    Go Worker     │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    Gmail API     │
                         └──────────────────┘
