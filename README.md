
# 👁️‍🗨️ **FaceEntry: Smart Face Recognition Access Control**

> _Welcome to the future of secure, seamless visitor authentication!_

---

## 🚀 **Project Infrastructure **


![Screenshot (156)](https://github.com/user-attachments/assets/4356bf0c-b34d-45e4-b75c-b756598c9a03)

## 🚀 **Project Overview**
- **AWS Infrastructure:**
  - Two **S3 Buckets**:
    - 🗂️ `Employee Pictures`
    - 🗂️ `Visitor Pictures`
  - Created an **IAM Role** for Lambda with full access to:
    - 📊 **CloudWatch**
    - 🗃️ **DynamoDB**
    - 📦 **S3**
    - 🌐 **API Gateway**
  - Two **AWS Lambda Functions** (Python):
    - 🧑‍💼 **Employee Registration:** Upload employee images to S3 & store metadata in DynamoDB.
    - 🚪 **Visitor Authentication:** Upload visitor images, authenticate using AWS Rekognition.
  - **API Gateway** exposes `GET` and `PUT` endpoints linking Lambda functions.

- **Frontend:**
  - Built with **React**.
  - Image upload for employee & visitor photos.
  - Stylish **Dark Mode** and **Light Mode** toggle 🌗.

---

## ✨ **Features**

- 🔐 Secure employee image registration with DynamoDB tracking.
- 🆚 Real-time visitor face authentication using AWS Rekognition.
- 🎨 Sleek UI with dark/light themes.
- 🖼️ Image preview before upload.

---

## 🛠️ **How to Use**

1. **Employee Registration**  
   Upload employee photos through the UI; images save to S3 and metadata to DynamoDB.

2. **Visitor Authentication**  
   Upload visitor photos; AWS Rekognition matches faces and authenticates access.

---

## 🧰 **Tech Stack**

- **Frontend:** React, JavaScript, CSS  
- **Backend & AWS:**  
  - AWS Lambda (Python)  
  - AWS S3 (Employee & Visitor buckets)  
  - AWS DynamoDB  
  - AWS API Gateway  
  - AWS Rekognition  
  - IAM Roles & Policies

---
## 📸 App Screenshots

| Description                      | Dark Mode                                   | Light Mode                                  |
|---------------------------------|--------------------------------------------|---------------------------------------------|
| **Welcome Screen**               | ![Screenshot (2)](https://github.com/user-attachments/assets/f8a55cd8-e114-412b-b7c2-595fa91a24ed)| ![Screenshot (1)](https://github.com/user-attachments/assets/0dac63f8-b984-4df7-85df-9b88f1c20183)|
| **Authentication Success**       | ![Screenshot (3)](https://github.com/user-attachments/assets/96cadc02-ab5a-429d-9469-baf940854c95)| ![Screenshot (6)](https://github.com/user-attachments/assets/79e48f5b-c78b-448e-8e84-8e99d383e139)|
| **Authentication Failed**        | ![Screenshot (8)](https://github.com/user-attachments/assets/e2900240-11e7-4efb-9ce5-aec7ce16d05c)| ![Screenshot (9)](https://github.com/user-attachments/assets/0b98a402-c29e-43d4-a619-6e76bfc0033b)|

---

## ⚙️ **Setup Instructions**

1. Create two S3 buckets (employee and visitor images).
2. Create an IAM Role with full access to CloudWatch, DynamoDB, S3, API Gateway.
3. Deploy Lambda functions for employee registration & visitor authentication.
4. Setup API Gateway endpoints linked to Lambda.
5. Clone frontend repo & install dependencies:
   ```bash
   npm install
