# 🚀 Capstone Project: CI/CD Mastery  

## **📌 Project Scenario**  
A technology consulting firm is adopting a cloud architecture for its software applications. As a **DevOps Engineer**, my task was to design and implement a **CI/CD pipeline** using **Jenkins** to automate the deployment of a web application. The goal was to ensure:  
- **Continuous Integration (CI)**  
- **Continuous Deployment (CD)**  
- **Scalability and Reliability** of the applications  

---

## **🛠 Jenkins Server Setup**  

### **Installation Steps**  
1. **Update and Install Java** (Required for Jenkins)  
   ```bash
   sudo apt update
   sudo apt install openjdk-11-jdk -y

2. **Add Jenkins Repository and Install Jenkins**
  `
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt update
sudo apt install jenkins -y
  `
3. **Start and Enable Jenkins**
  `
  sudo systemctl start jenkins
  sudo systemctl enable jenkins
  `
4. **Access Jenkins**
Visit: http://<your-server-ip>:8080
Unlock Jenkins using:
`sudo cat /var/lib/jenkins/secrets/initialAdminPassword
`
## **Plugin Installation**
- Navigate to Manage Jenkins → Plugin Manager → Available
- Install the following plugins:
- Git Plugin
- Pipeline Plugin
- Docker Plugin
- GitHub Integration Plugin

## Security Measures
- Enable Admin Authentication
- Disable Anonymous Access
- Install Credentials Binding Plugin for secure key management

## **🔗 Source Code Management (SCM) Integration**
GitHub Integration with Jenkins

Add GitHub credentials in Manage Jenkins → Credentials
Create a Jenkins Pipeline job and select Git as SCM
Add Webhooks in GitHub:
Go to Repository → Settings → Webhooks
Add webhook URL:
`
http://<jenkins-server-ip>:8080/github-webhook/
`
## Jenkins Pipeline for web application
### **Pipeline SCript**
 - Refer to the jenkinsfile

# **📌 Conclusion**
This project successfully demonstrated a complete CI/CD pipeline using Jenkins, integrating source control, automated builds, unit tests, and Docker deployment. The experience strengthened my DevOps skills in automation, infrastructure security, and containerization.
 
