# Secure – Data Security and Compliance Project

---

## Project Overview

This project focuses on securing sensitive data and ensuring compliance using **Microsoft Azure technologies**. It leverages **Azure Active Directory (AAD)**, **Azure Key Vault**, and **Multi-Factor Authentication (MFA)** to implement robust access control and data protection.

---

## Architecture

The system architecture illustrates the interaction between **AAD**, **Azure Key Vault**, and **MFA** for secure access and data management.  


---

## Configuration Details

### 1. Role-Based Access Control (RBAC)

| Role         | Description                        | Assigned To        |
|--------------|------------------------------------|------------------|
| Owner        | Full control over resources        | IT Admin Group    |
| Contributor  | Manage resources but cannot assign roles | Development Team |
| Reader       | View resources without making changes | Audit and Compliance |

### 2. Access Policies for Azure Key Vault

| Access Type         | Permissions          | Assigned To        |
|--------------------|-------------------|------------------|
| Key Access          | Get, List, Delete  | IT Admin Group    |
| Secret Management   | Get, List, Update  | Development Team  |
| Certificate Access  | Get, List          | Security Team     |

### 3. Multi-Factor Authentication (MFA)

- **Policy Name:** Enforce MFA for Sensitive Resources  
- **Scope:** Applies to all users accessing Azure Portal and Key Vault  
- **Conditions:**  
  - Require MFA for all sign-ins  
  - Apply MFA only for critical resource groups  

---

## Implementation Steps

1. **Configure Azure Active Directory**  
   - Add users and groups  
   - Assign roles using Access Control (IAM)  

2. **Secure Sensitive Data with Azure Key Vault**  
   - Store secrets like API keys and connection strings  
   - Define access policies for roles and groups  

3. **Enforce Multi-Factor Authentication**  
   - Create a Conditional Access policy in AAD  
   - Enable MFA for all defined scopes  

4. **Monitor and Maintain Compliance**  
   - Enable Microsoft Defender for Cloud  
   - Generate compliance reports using Azure Compliance Manager  

---

## Outcome

- **RBAC Implementation:** Defined granular access to Azure resources  
- **Data Security:** Secrets and keys securely stored in Azure Key Vault  
- **Enhanced Authentication:** MFA ensures secure access to critical resources  
- **Compliance Monitoring:** Tools like Microsoft Defender and Compliance Manager provide continuous security assessments  

---

Author: Karanam Sumanth, B.E. in Information Technology, 2025
