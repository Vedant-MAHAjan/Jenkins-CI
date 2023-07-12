# Continuous Integration Pipeline using Jenkins

## Flow of pipeline

1. Checkout the code from git repository
2. Build the artifact using Maven
3. Test the artifact using Maven
4. Perform check style analysis on the code
5. Perform SonarQube analysis to check for bugs, vulnerabilities
6. Test Quality Gates based on the SonarQube results
7. Upload artifact on Nexus Repository with proper timestamp


## Execution

#### - Launch an EC2 instance and execute scripts for Jenkins installation
#### - Check the status of the Jenkins service
  
![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/7dc8fae4-ef1f-4daf-8fdb-a54209fb7554)

Note - Add plugins and Tool configuration for all the tools (Nexus, Sonarqube, git, pipeline maven integration plugin and build timestamp)


#### - Launch an EC2 instance and execute scripts for Nexus installation
#### - Setup new username and password
  
![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/56b24a03-f935-472a-8cac-b66a10d01135)

#### - Launch an EC2 instance and execute scripts for SonarQube installation
#### - Log in using username as "admin" and password also as "admin"

![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/098ce041-d511-408b-af0d-74433e7aebc1)

#### - Integrate SonarQube with Jenkins by adding a URL of the SonarQube service
#### - The URL consists of the private IP of the SonarQube instance

![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/29b03980-3701-48c4-b495-14e79caa35d3)

#### - Create a quality gate on SonarQube as a threshold for the number of bugs

![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/3ad7929f-a2f3-44e0-9a6c-26c82f8bdf25)

#### - Create a webhook that will pass the results of the report from SonarQube to Jenkins

![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/6bce8b3b-f7bb-45d4-9234-8ad1ea45ea20)

#### - Create a Nexus repository '''vprofile-repo''' that will store the artifact
  
![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/e819b827-fb03-4b21-9034-2deb292825cd)

#### - The artifact is stored in the repository with the appropriate timestamp

![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/aa013b67-fab5-460e-b04b-9703b6ec240a)

#### - Check the successful pipeline build on Jenkins
  
![image](https://github.com/Vedant-MAHAjan/Jenkins-CI/assets/88843623/17677f9e-fdb6-42e2-a874-d935feb03d01)


