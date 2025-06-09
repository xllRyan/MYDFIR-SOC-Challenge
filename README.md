# MYDFIR-SOC-Challenge

This is a 30 days challenge from MYDFIR. 
This project provides a practical, hands-on environment to simulate the daily tasks and challenges faced by Security Operations Center (SOC) analysts. It is ideal for both beginners and those with industry certifications looking to strengthen their real-world skills in threat detection, incident response, SIEM tools, and security strategy development.

🛠️ Tools Used
Elastic Stack (Elasticsearch, Logstash, Kibana)
Sysmon
Mythic (C2 Framework)
OS Ticket
Vultr Cloud Hosting

🎯 Main Objectives
Design a logical network diagram
Setup and configure Elastic Stack (ELK)
Simulate, detect, and investigate common attacks (malware, SSH/RDP brute force)
Create alerts and dashboards in Kibana
Integrate a ticketing system for alert tracking

📅 Timeline Breakdown
Week 1: ELK Stack & Log Ingestion
Introduction to ELK components
Setup and configuration of ELK on Vultr
Ingest logs using Sysmon

Week 2: Brute Force Detection
Simulate SSH and RDP brute force attacks
Setup target servers (Ubuntu for SSH, Windows for RDP)
Configure dashboards and alerts in Kibana

Week 3: Command & Control (C2) Simulation
Introduction to command and control techniques
Deploy and configure a Mythic C2 server
Launch attacks from a Kali Linux hacker machine
Analyze post-exploitation behavior

Week 4: Ticketing System & Alert Management
Setup and integrate OS Ticket
Link alerts from Elastic to create tickets
Investigate high-level alerts through the ticketing workflow


🧭 Network Architecture Overview
This logical diagram outlines the architecture deployed in a Virtual Private Cloud (VPC) hosted on Vultr.

Components:
SOC Analyst’s Laptop: Accesses Elastic Stack via web interface for monitoring and investigation.
VULTR: Cloud platform hosting all infrastructure.
VPC (192.168.0.0/24): Private network for internal communication between servers.
Elastic & Kibana Server: Core ELK services for log storage, visualization, and alerting.
Fleet Servers: Forward logs from various endpoints to Elastic.
Windows Server (RDP Enabled): Simulated target for brute force and RDP attacks.
Ubuntu Server (SSH Enabled): Simulated target for SSH attacks.
Hacker Laptop (Kali Linux): Used to launch attacks and connect to the C2 server.
C2 Server (Mythic): Manages compromised systems and post-exploitation activities.
OS Ticket Server: Receives alerts from Elastic to generate investigation tickets.
Internet Gateway: Allows external access to the lab environment.

What is ELK?

The ELK Stack consists of Elastic, Logstash, and Kibana, which work together to handle and analyze large volumes of data, particularly logs.

Elasticsearch is the core of the stack. It is a distributed search and analytics engine that stores and indexes data in a way that allows for fast search and retrieval. When data is ingested, Elasticsearch organizes it, enabling users to perform quick and complex searches.

Logstash acts as the data pipeline. It ingests data from either Beats or Elastic Agents, processes and transforms it, and then sends it to Elasticsearch for storage. Logstash can pull data from many different places, apply filters to clean or enhance it, and then output the processed data to Elasticsearch or other destinations.

Kibana provides the visual layer. It is a web interface that allows users to interact with the data stored in Elasticsearch. Through Kibana, users can create dashboards, perform searches, and visualize data trends and patterns, making it easier to gain insights and monitor systems.

In summary, Logstash collects and processes data, Elasticsearch stores and indexes it, and Kibana visualizes it, working together seamlessly to provide a powerful data analysis platform.
