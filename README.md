
# 🚀 Enable Cross-Region Backup Replication for EC2 using AWS Backup

## 🎯 Objective
This project demonstrates how to automatically back up an EC2 instance using AWS Backup and replicate those backups to another AWS region for enhanced durability and disaster recovery.

---

## 🛠️ Project Workflow

### 1. EC2 Instance Setup
- Launched an EC2 instance in the **primary AWS region**.
- Uploaded sample files to test data integrity during backup and recovery.

![EC2 Instance Details](./screenshots/ec2_instance_details.png)

---

### 2. AWS Backup Vaults
Created two backup vaults:
- One in the **source region** for initial backup storage.
- One in the **destination region** for cross-region replication.

#### 🔹 Source Vault:
![Source Backup Vault](./screenshots/1_Source_Backup_Vault.png)

#### 🔹 Destination Vault:
![Destination Backup Vault](./screenshots/2_Destination_Backup_Vault.png)

---

### 3. AWS Backup Plan Creation
- Created a backup plan with daily backup frequency.
- Assigned the EC2 instance as a resource.
- Enabled lifecycle rules to transition backups to cold storage after 30 days.

![Backup Plan Configuration](./screenshots/5_Backup_Plan_CrossRegion_Configuration.png)

---

### 4. Cross-Region Backup Replication
- Configured the backup plan to replicate backups to another AWS region.
- Selected a destination vault and defined the copy frequency and retention.

---

### 5. Backup Jobs Validation
- Triggered an on-demand backup for immediate testing.
- Verified job completion status in the **Backup Jobs** section.

![Backup Jobs Successful](./screenshots/3_Backup_Jobs_Successful_Completion.png)

---

### 6. Cross-Region Recovery Point
- Switched to the **destination region**.
- Verified that the replicated recovery point was created in the vault.

![Recovery Point in Destination](./screenshots/4_EC2_Recovery_Point_Destination.png)

---

## 🔍 Why AWS Backup?

AWS Backup is a fully managed backup service that:
- Automates and centralizes backup across AWS services.
- Supports compliance, auditing, and retention policies.
- Enables **cross-region replication** to protect from regional failures.
- Ensures secure and reliable **disaster recovery** strategies.

With AWS Backup, you get **policy-driven backups**, **fine-grained control**, and **cost-effective cold storage transition** options — all within the AWS ecosystem.

---

## 📄 Summary Report

A detailed PDF summary report is included in this repository:  
👉 [Summary_Report.pdf](./Summary_Report.pdf)

---

## ✅ Conclusion

This project showcases how a well-structured AWS Backup plan, combined with cross-region replication, can help build **resilient and disaster-ready cloud infrastructure**.

If you found this helpful or have questions, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/your-profile/) or check out more projects in my GitHub profile.

---

### 📌 Tags
`AWS` `EC2` `AWS Backup` `Cross-Region Replication` `Disaster Recovery` `DevOps` `Cloud Projects`

---
