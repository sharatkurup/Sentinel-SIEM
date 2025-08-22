# 🛡️ Home Lab SIEM Project – Microsoft Sentinel

## 📄 About the Project
This is a home lab I built to get hands-on experience with **Microsoft Sentinel**.  
The goal was to simulate a realistic IT environment and demonstrate **log collection, threat detection, and alerting workflows**.  

---

## 🏢 Scenario
A **mid-size fintech company** with:  
- Windows servers for internal apps  
- Linux servers running backend services  
- Web application with a customer database in Azure  
- Employees using Windows 10 devices  
- Azure AD managing user logins  

**Threats simulated:**  
- Brute-force attempts on employee accounts  
- Unauthorized access to the customer database outside business hours  
- Failed admin logins from foreign IPs  

---

## ⚙️ How I Built It

### 1️⃣ Setting up Sentinel
- Created a **Log Analytics Workspace** in Azure (free tier)  
- Enabled **Microsoft Sentinel** for log collection and analysis  

### 2️⃣ Dummy Logs
Used sample and generated logs to simulate real activity:  
- **Windows Event Logs:** Login successes/failures, admin actions  
- **Linux Syslogs:** SSH access attempts, file permission changes  
- **Web Server Logs:** Simulated customer access and attacks  

### 3️⃣ Detection Rules
Created **analytics rules using Kusto Query Language (KQL)**:  
- Multiple failed logins from the same IP  
- Logins outside business hours  
- Admin account failures  
- Suspicious IP addresses accessing sensitive data  

### 4️⃣ Dashboards
Built **Sentinel Workbooks** to visualize:  
- 🔺 Top offending IPs  
- 📊 Login failures over time  
- ⚠️ High-risk alerts and events  

### 5️⃣ Alerts
Configured **email alerts** for high-risk events to mimic SOC escalation.

---

## 🎯 What I Learned
- Log ingestion from multiple sources in Sentinel  
- Writing detection rules with KQL  
- Visualizing events and creating dashboards  
- Mapping SIEM monitoring to security frameworks:  
  - **NIST CSF:** Detect & Respond  
  - **ISO 27001:** Incident Management & Operations Security  
  - **SOC 2:** Logging and Monitoring Controls  

---

## 🚀 Next Steps
- Add **automated responses** using Azure Logic Apps  
- Connect **threat intelligence feeds** for real-time detection  
- Extend to **multi-cloud or hybrid environments**  
- Run simulated incident scenarios for SOC readiness  

---

## 🛠️ Tools Used
- Microsoft Azure (Free Tier)  
- Microsoft Sentinel  
- Kusto Query Language (KQL)  
- Dummy Windows/Linux logs (public datasets and scripts)  
- Sentinel Workbooks for dashboards  

---

## 📂 Deliverables
- Risk & event dashboards  
- Detection rules (KQL queries)  
- Sample alerts and email notifications  
- Documentation mapping to NIST CSF, ISO 27001, SOC 2  

