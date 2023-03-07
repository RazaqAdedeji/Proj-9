## Project 9: Continuous Integration Pipeline for Tooling Website

- Install Jenkins server

'sudo apt update'

'sudo apt install default-jdk-headless'

- Install Jenkins

'wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

'sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'

'sudo apt update'

'sudo apt-get install jenkins'

'sudo systemctl status jenkins'

![alt text](./images/1%20jenkins%20status.png)

- Perform initial Jenkins setup.
From your browser access http://<Jenkins-Server-Public-IP-Address-or-Public-DNS-Name>:8080

![alt text](./images/2%20unlock%20jenkins.png)

![alt text](./images/3%20admin%20password.png)

![alt text](./images/4%20jenkins%20ready.png)

- Step 2 – Configure Jenkins to retrieve source codes from GitHub using Webhooks

![alt text](./images/5%20webhook.png)

- Go to Jenkins web console, click "New Item" and create a "Freestyle project"

![alt text](./images/6%20Build%201.png)

![alt text](./images/7%20console%20output.png)

- Save this configuration and go ahead, change something in README.MD file in your GitHub Tooling repository

![alt text](./images/8%20Edit%20readme.png)

![alt text](./images/9%20edit%20readme.png)

'ls /var/lib/jenkins/jobs/tooling_github/builds/<build_number>/archive/'