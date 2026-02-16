#  Money Transfer API – Postman Collection

A professional Postman collection for testing the ** Money Transfer API ** of NewrozTech.  
This collection supports secure authentication and financial transactions between System, Agent, Customer, and Merchant roles.



# API Configuration

**Base URL**https://mta.newroztech.com/api 

**Authentication Keys**

| Key | Value |
|-----|------|
SYSTEM | b82439df1c92a7fe504bf23da918e6f1 |
SECRET_KEY | e97b4ca15fd2b3086c1e4af98b72d503 |

These keys must be configured in Postman environment before executing APIs.

---

#  Collection Modules

The collection includes the following functional modules:

- Authentication
- User Management
- Wallet & Balance
- Money Transfer
- Deposit & Withdraw
- Commission Management
- Transaction History
- System Virtual Balance

---

#  Setup Instructions

## 1️ Import Files into Postman

Import the following files:
Money-Transfer-API.postman_collection.json
Money-Transfer-API.postman_environment.json


Postman → Import → Select both files

---

#  Environment Setup

After importing:

1. Open **Postman**
2. Go to **Environments**
3. Select: `Money Transfer API Environment`
4. Set values:

| Variable | Value |
|----------|------|
base_url | https://mta.newroztech.com/api |
system_key | b82439df1c92a7fe504bf23da918e6f1 |
secret_key | e97b4ca15fd2b3086c1e4af98b72d503 |

Save environment.

---

#  Authentication

All secured APIs use **Bearer Token** authentication.

### Login API

After successful login, token is automatically stored: {{admin_token}}
Used in headers:Authorization: Bearer {{admin_token}}

---

#  User Management APIs

| API | Method | Description |
|-----|-------|------------|
/user-list | GET | Retrieve all users |
/search-user-by-email | GET | Search by email |
/search-user-by-id | GET | Search by ID |
/user-create | POST | Create user |

---

#  Wallet & Balance APIs

| API | Method | Description |
|-----|-------|------------|
/balance-check | GET | Check wallet balance |
/transaction-history | GET | Transaction list |
/transaction-details | GET | Transaction info |

---

#  Money Transfer APIs

| API | Method | Description |
|-----|-------|------------|
/send-money-customer-to-customer | POST | Customer transfer |
/withdraw-customer-to-agent | POST | Withdraw to agent |
/payment-customer-to-merchant | POST | Merchant payment |

---

#  Deposit APIs

| API | Method | Description |
|-----|-------|------------|
/deposit-system-to-agent | POST | System → Agent |
/deposit-system-to-customer | POST | System → Customer |
/deposit-agent-to-customer | POST | Agent → Customer |

---

#  Commission APIs

| API | Method | Description |
|-----|-------|------------|
/commission-listing | GET | Commission list |
/commission-create | POST | Create commission |

---

#  System Virtual Balance APIs

| API | Method | Description |
|-----|-------|------------|
/admin-create-virtual-money | POST | Create system money |
/system-virtual-balance | GET | System balance |

---

#  Recommended Test Flow

Execute APIs in this order:

1. Login  
2. User Create  
3. Deposit  
4. Balance Check  
5. Money Transfer  
6. Withdraw  
7. Commission  
8. Transaction History  
9. System Balance  

---

#  Testing & Validation

The collection includes automated tests:

- Status code validation
- Response structure validation
- Data integrity checks
- Token handling
- Financial value checks

Example:

pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});

All identified issues during API testing are documented in: Self Hema Bug List For MT-API.XLSX 

The report includes:

- Endpoint
- Request
- Expected Result
- Actual Result
- Severity
- Status

---

# Project Files

Money-Transfer-API.postman_collection.json
Money-Transfer-API.postman_environment.json
Bug_Report_Money_Transfer_API.xlsx
README.md


---

#  QA Information

Tested By: Tasnia Sultana Hema
Project: Money Transfer API  
Company: NewrozTech  
Testing Type: API Functional & Validation Testing  

---

#  Ready to Use

Import → Configure Environment → Login → Execute APIs 


