# API-Testing-Suite
# 📝 Notes API – Postman Automated Test Suite

This repository contains a **Postman test collection** for the **Notes API** along with an environment file for dynamic variable handling and testing.

---

## 🚀 Project Overview

This project was developed as part of automating test scenarios for a RESTful Notes API. It covers:

- ✅ Functional test cases for all CRUD operations  
- ⚠️ Negative test cases with dynamic value injection  
- 🧪 Automated assertions using Postman test scripts  
- 🌐 Environment-specific variables for seamless execution  

---

## 📁 Files Included

- `notes-api.postman_collection.json` – Postman Collection with 21 test cases  
- `env.postman_environment.json` – Postman Environment setup for local testing  

---

## ✅ Features Tested

### 📌 Create Note
- Validations for missing fields  
- Long titles  
- Invalid content types  

### 📌 Read Notes
- Single and all notes retrieval  
- Invalid ID handling  

### 📌 Update Note
- Valid updates  
- Invalid or missing data scenarios  

### 📌 Delete Note
- Successful deletion  
- Deletion with invalid/non-existing IDs  

### ⚠️ Edge Cases
- XSS injection  
- SQL injection patterns  
- Large payloads  

---

## 🧪 How to Run Tests

### 1. Import Collection & Environment

Open **Postman** and import the following files:

- `notes-api.postman_collection.json`  
- `env.postman_environment.json`  

### 2. Select Environment

Select `env` from the environment dropdown in Postman.

### 3. Hit "Run"

Use **Collection Runner** in Postman or use **Newman** CLI:

```bash
newman run notes-api.postman_collection.json -e env.postman_environment.json


## 📌 Requirements

To run this project and execute the test suite, make sure you have the following installed:

### 🛠️ Tools

- [**Postman**](https://www.postman.com/downloads/) – API testing tool (version 10 or higher recommended)
- [**Node.js & npm**](https://nodejs.org/) – Required for running Newman from the command line
- [**Newman**](https://www.npmjs.com/package/newman) – CLI Collection Runner for Postman

### 📥 Install Newman

Install Newman globally using npm:

```bash
npm install -g newman
