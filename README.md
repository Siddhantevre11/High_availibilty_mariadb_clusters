
# High Availability MariaDB Clusters with Galera on AWS ☁️

## 📌 Project Overview
This project implements a high-availability, fault-tolerant MariaDB cluster using **Galera** on **AWS EC2** instances. Two deployment modes are evaluated:
- **Manual CLI-based setup** using `mysqldump` and replication scripts
- **Managed setup** with **Galera Manager**

## 🎯 Objectives
- Achieve real-time replication with no single point of failure
- Benchmark replication latency and failover response
- Automate backups and monitor cluster health via AWS CloudWatch

## 🧱 Architecture
- **3-node EC2 cluster** using t3.micro instances (Ubuntu)
- **Galera synchronous replication**
- **Elastic IPs** for persistent addressing
- **S3** for automated backups

## 📊 Datasets Used
- [SMS Corpus (10MB)](https://github.com/kite1988/nus-sms-corpus/blob/master/smsCorpus_en_sql_2015.03.09_all.zip)
- [E-Commerce Sales (90MB)](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data)
- [Crime Data (180MB)](https://catalog.data.gov/dataset/crime-data-from-2020-to-present)

## 🛠️ Features
- Synchronous replication across all nodes
- Real-time monitoring of replication via Galera Manager
- CloudWatch dashboards for CPU/network load analysis
- Automated failover and manual simulation of node shutdown

## 🧪 Key Findings
- Galera reduced replication lag even under heavy loads
- Manual setups failed under 180MB+ data inserts
- Galera Manager offered easy cluster management but limited provisioning features

## 📉 Cost Comparison
- Benchmarked AWS EC2 vs Azure B2ms nodes
- Identified regional deployment and licensing constraints

## 📘 References
- [Galera Cluster Docs](https://galeracluster.com/library/documentation/)
- [MariaDB Config Guide](https://galeracluster.com/library/documentation/install-mariadb.html)
- [mysqldump Manual](https://dev.mysql.com/doc/refman/8.4/en/mysqldump.html)

---

**Author:** Siddhant | [LinkedIn](https://www.linkedin.com)  
