# 🚀 Serverless Project Deployment on AWS

## 📌 Project Overview

This project demonstrates the deployment of a **secure, scalable Serverless Web Application on AWS** using managed services. The architecture consists of a static frontend, REST API, serverless backend, and NoSQL database.

### Architecture Flow

```text
User
  |
  v
Route 53
  |
  v
ACM + AWS WAF
  |
  v
CloudFront
  |
  v
S3 (HTML/CSS/JS)
  |
  | HTTPS API Calls
  v
API Gateway
  |
  v
AWS Lambda
  |
  v
DynamoDB
```

---

## 🏗️ Architecture

```text
                    👤 USER
                       |
                       v
                +-------------+
                | Route 53    |
                |    DNS      |
                +------+------+
                       |
                       v
             +-------------------+
             | ACM + AWS WAF     |
             | Security Layer    |
             +---------+---------+
                       |
                       | HTTPS
                       v
                +-------------+
                | CloudFront  |
                |     CDN     |
                +------+------+
                       |
                       v
                +-------------+
                |     S3      |
                |   Static    |
                |  Frontend   |
                | HTML/CSS/JS |
                +------+------+
                       |
                       | API Calls
                       v
                +-------------+
                | API Gateway |
                |   REST API  |
                +------+------+
                       |
                       v
                +-------------+
                |   Lambda    |
                |  Functions  |
                +------+------+
                       |
                       | Read / Write
                       v
                +-------------+
                |  DynamoDB   |
                | NoSQL DB    |
                +-------------+
```

---

## ☁️ AWS Services Used

| AWS Service | Purpose |
|---|---|
| **Route 53** | DNS and domain management |
| **ACM** | SSL/TLS certificate |
| **AWS WAF** | Web application protection |
| **CloudFront** | Global CDN and content delivery |
| **S3** | Static frontend hosting |
| **API Gateway** | REST API |
| **Lambda** | Serverless backend |
| **DynamoDB** | NoSQL database |
| **IAM** | Service permissions |

---

## 🔄 Application Flow

```text
1. User accesses the application domain
2. Route 53 resolves the domain
3. ACM provides HTTPS security
4. AWS WAF filters configured web traffic
5. CloudFront delivers frontend content
6. S3 stores HTML, CSS and JavaScript
7. Frontend sends HTTPS requests to API Gateway
8. API Gateway invokes Lambda functions
9. Lambda reads/writes employee data in DynamoDB
10. JSON response is returned to the user
```

---

## 🔌 API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| **POST** | `/employeeData` | Insert employee data |
| **GET** | `/employeeData` | Retrieve employee data |

### API Flow

```text
Frontend
   |
   v
API Gateway
   |
   v
Lambda
   |
   v
DynamoDB
```

### DynamoDB

```text
Table Name : employeeData
Primary Key: employeeid
Type       : String
```

---

## 🔐 Security

- HTTPS using **AWS Certificate Manager**
- Web protection using **AWS WAF**
- IAM roles for AWS service permissions
- CORS enabled for API communication
- Frontend hosted separately from backend
- Database accessed through Lambda
- No AWS credentials stored in source code

---

## 🎯 Key Features

- Serverless architecture
- Static website hosting using S3
- Global content delivery using CloudFront
- Custom DNS using Route 53
- HTTPS using ACM
- Web application protection using WAF
- REST API using API Gateway
- Serverless backend using Lambda
- NoSQL database using DynamoDB
- Scalable and managed AWS services
- No traditional server management

---

## 🛠️ Technologies

`AWS` `Serverless` `S3` `CloudFront` `Route 53` `API Gateway` `Lambda` `DynamoDB` `IAM` `WAF` `Linux` `Git` `GitHub` `Python` `REST API`

---

## 🔍 What I Learned

Through this project, I gained practical experience in:

- Serverless AWS architecture
- S3 static website deployment
- CloudFront CDN configuration
- Route 53 DNS
- ACM and HTTPS
- AWS WAF
- API Gateway REST APIs
- Lambda functions
- DynamoDB
- IAM permissions
- CORS configuration
- API testing
- AWS service integration
- End-to-end cloud deployment

---

## 🚀 Future Improvements

- Terraform / CloudFormation
- GitHub Actions CI/CD
- Jenkins CI/CD
- CloudWatch monitoring
- API authentication
- Amazon Cognito
- Automated testing
- AWS Secrets Manager

---

## 👨‍💻 Author

**Vijay Kumar Sammeta**

**B.Tech – Computer Science / Information Technology**

### Skills

`AWS` `DevOps` `Linux` `Git` `GitHub` `Python` `Cloud` `Serverless`

---

## ⭐ Project Highlights

**Route 53 → ACM/WAF → CloudFront → S3 → API Gateway → Lambda → DynamoDB**

A complete serverless AWS application demonstrating **secure content delivery, REST API integration, serverless backend processing, and NoSQL database storage**.
