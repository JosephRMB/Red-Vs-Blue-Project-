# Red-Vs-Blue-Project-
- Red and Blue team exercise project done for the University of California Davis in collaboration with 2u/Edx
- This repository consists of documentation, personal notes, and resources used for the Red Vs Blue Project created, supervised, and supported by the University of California Davis in collaboration with 2u/Edx bootcamps. 
- This project was completed in the early summer of 2020.
- The emails, virtual machines, and credentials used for this project were all provided by UC Davis and 2u Edx to take advantage of the free runtime credits for new accounts made in Microsoft Azure Cloud. 
- All virtual machines, virtual networks, and resource groups used in this project are now decomissioned in order to prevent real monetary charges to leak out of using Microsoft's PaaS (Azure Cloud) during the time - the course requiring this project was being taken. 
- Some screenshots of terminals and Azure UI may be missing outdated, or pulled from instructional material due to signiificant changes made since the time of completion.
- Screenshots pulled from instructional material will be marked with a "*"

OBJECTIVES 
1. Utilize Azure Cloud services to create a resource group consisting of two interconnected virtual networks hosting 4 virtual machines in total 
- A virtual machine to serve as an SSH jumpbox to act as a one-way tunnel to connect to the secure resource group
- A "Metasploitable" capstone machine left intentionally vulnerable (but closed off to the open internet) meant to be scanned and pentested on
- A RedBox Kali-Linux hosting machine with all the tools necessary to run scans and exploits on the vulnerable capstone machine 
- A BlueBox Elk-Stack hosting machine meant to utilize Kibana, Logstash, and Elastisearch to be a SIEM monitoring the traffic/communication between the RedBox and the Capstone 
The resource groups and virtual networks will be configured in a way to only allow the BlueBox to have secure open access to the internet.
Configurations are made so that the Jump-Box has SSH access to all 3 Virtual Machines via a secure tunnel 
Configurations are also made to allow open communication between the vnet containing the RedBox and Capstone to the vnet containing ONLY the BlueBox Elk-Stack host


2. Configure the Jump-Box machine to utilize Ansible playbooks to automate the deployment and overhead of Docker containers to be hosted on the other 3 virtual machines. 
- Make configuratuions on ansible to be compatible with python3
- Use a YAML script to setup the Capstone Metasploitable
- Use a YAML script to setup the RedBox Kali-Linux host
- Use a YAML script to setup the BlueBox Elk-Stack host. 
Verify the Capstone Metasploitable's DVWA is available 

3. Setup Filebeat and Metric Beat using YAML (ansible playbooks) on the Capstone and its DVWA configuring them to send data to the Elk-Stack host.

4. Verify the functionality of Kibana by plugging in sample log data.

5. Prepare the environments for a Red vs Blue CTF exercise done by the individual
   - Restart services for metricbeat
   - Restart services for filebeat
   - Add and configure packet beat

6. Utilize tools to conduct the RedTeam sided CTF on the capstone machine. Tools and resources used include...
   - Firefox (any browser)
   - Hydra
   - Nmap
   - John the Ripper
   - Metasploit
   - MSFVenom
  
7. Utilize tools to conduct the BlueTeam sided review of CTF activity done during the RedTeam attack
   - Identify the source IP of traffic
   - Identify requests for important/hidden directories
   - Identify Brute Force attacking traffic
  
8. Write a final report and presentation. The presentation and report has already been submitted to the corresponding professor of my cohort. This repo as mentioned earlier serves as finalized documentation.
