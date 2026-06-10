# DummyJSON E-commerce API Testing Project

## Overview

This repository contains an API testing portfolio project for an e-commerce style REST API. The project is built around the DummyJSON API and covers product catalog, product search, product category, cart, user, and authentication flows.

The main goal of this project is to demonstrate a structured QA approach for REST API testing using Postman, including positive scenarios, negative scenarios, response validation, JSON field validation, and basic automated assertions.

## Application Under Test

**API:** DummyJSON  
**Base URL:** `https://dummyjson.com`  
**Test Type:** REST API Functional Testing  
**Tool:** Postman  
**Optional CLI Tool:** Newman

## Scope

The project covers the following API areas:

- API health check
- Authentication
- Product listing
- Product search
- Product details
- Product categories
- Product create/update/delete simulation
- Cart listing and cart management simulation
- User listing, user details, and user search
- Negative testing for invalid IDs and invalid login

## Repository Structure

```text
dummyjson-api-testing-project/
├── .github/
│   └── workflows/
│       └── api-tests.yml
├── docs/
│   ├── API_Test_Strategy.md
│   ├── Bug_Report_Samples.md
│   ├── Postman_Test_Script_Notes.md
│   ├── Test_Cases.md
│   └── Test_Plan.md
├── learning-notes-bangla/
│   └── Interview_Preparation_Bangla.md
├── postman/
│   ├── DummyJSON_Ecommerce_API_Tests.postman_collection.json
│   └── DummyJSON_QA_Environment.postman_environment.json
├── reports/
│   ├── Test_Execution_Summary.md
│   └── Risk_And_Improvement_Notes.md
├── .gitignore
├── package.json
└── README.md
```

## How to Run in Postman

1. Open Postman.
2. Click **Import**.
3. Import the collection:
   - `postman/DummyJSON_Ecommerce_API_Tests.postman_collection.json`
4. Import the environment:
   - `postman/DummyJSON_QA_Environment.postman_environment.json`
5. Select **DummyJSON QA Environment** from the environment dropdown.
6. Open the collection.
7. Click **Run collection**.
8. Review passed/failed test results.

Important: Run the collection in order. The valid login request saves the access token into the environment, and the authenticated user request uses that token.

## How to Run with Newman

Install dependencies:

```bash
npm install
```

Run API tests:

```bash
npm test
```

Generate a CLI + HTML report:

```bash
npm run test:report
```

## Test Coverage Summary

| Area | Covered |
|---|---|
| Health check | Yes |
| Authentication | Yes |
| Product listing | Yes |
| Product details | Yes |
| Product search | Yes |
| Category filtering | Yes |
| Product create/update/delete simulation | Yes |
| Cart APIs | Yes |
| User APIs | Yes |
| Negative testing | Yes |
| Response time validation | Yes |
| JSON response validation | Yes |
| GitHub Actions workflow | Yes |

## Key QA Validations

The Postman collection validates:

- HTTP status codes
- Response time
- JSON response format
- Required response fields
- Data type consistency
- Search response structure
- Pagination metadata
- Auth token handling
- Negative responses for invalid input
- Simulated create/update/delete responses

## Project Notes

DummyJSON is a mock REST API. Create, update, and delete requests are simulated, meaning they return expected responses but do not permanently modify the server data. This behavior is documented as a mock API limitation and is included in the test notes.


.
