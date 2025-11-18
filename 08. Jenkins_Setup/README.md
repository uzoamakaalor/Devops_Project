# Jenkins Setup on Ubuntu EC2 Instance

This documentation demonstrates how to set up a Jenkins server on an Ubuntu EC2 instance in AWS and configuring the security group to allow external access.
 


## Installation Steps

**Step 1** Update System Packages

`sudo apt update`

![](./images/01.png)

**Step 2**  Install Java (OpenJDK)

JDK stands for ***Java Development Kit**, It is an open software development enviroment used for the development of Java Applications, and it is required for Jenkins because Jenkins runs on Java and depends on it to function.

![](./images/02.png)

Confirm Java is installed correctly and the version installed:
![](./images/02i.png)


**Step 3**  Add Jenkins Repository & Install Jenkins

On Ubuntu, the default package repository does not include Jenkins. Adding the Jenkins repository tells Ubuntu where to download Jenkins and ensures it installs the latest official version.

![](./images/03.png)

Verify Jenkins Status 
![](./images/03i.png)

JENKINS INSTALLED SUCCESSFULLY!


### SECURITY GROUP CONFIRGURATION

By default, Jenkins listens on port **8080**. An inbound rule for this port must be added to the security group where Jenkins is hosted to allow external access.

![](./images/04i.png)


#### Initial Setup
To access the Jenkins server, enter the EC2 instance’s public IP address followed by port 8080 in my browser.
![](./images/05.png)



On my browser
![](./images/05i.png)


To unlock Jenkins, I ran the command ` sudo cat /var/lib/jenkins/secrets/initialAdminPassword ` to get the password. 



Jenkins is lauched on my browser. 

![](./images/06.png)


Account setup on my Jenkins Server as well.

![](./images/06i.png)


Jenkins now ready and successfully installed!

![](./images/07.png)

![](./images/07i.png)





