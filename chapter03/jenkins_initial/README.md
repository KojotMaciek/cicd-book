# Preparation:
- creating local volume where the Jenkins home will be mapped:
	- mkdir ~/docker_volumes/jenkins_home

# Run docker Jenkins image:
- docker run -d -p 8080:8080 \\
  -v ~/docker_volumes/jenkins_home:/var/jenkins_home \
  --name jenkins jenkins/jenkins

# Access to Jenkins
- Open browser on the local machine: http://localhost:8080

# Start configuration
- Admin password can be found in the Jenkins logs:
	- docker logs jenkins 
