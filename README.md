# dat-infrastructure

# DAT Infrastructure uses Docker 

Use docker-compose to run any of the tools.

To run a container:

    docker-compose up

- Use -d for detached mode

To remove the container:

    docker-compose down


# Artifactory setup

Using docker

Links |
------| 
https://www.jfrog.com/confluence/display/RTF6X/Installing+on+Linux+Solaris+or+Mac+OS#InstallingonLinuxSolarisorMacOS-ManualInstallation|
https://www.jfrog.com/confluence/display/RTF6X/Installing+Artifactory|
------


- Step 1: Download artifactory CPP Comunity Edition from here https://bintray.com/jfrog/product/JFrog-Artifactory-Cpp-CE/view
- Step 2: Make sure Java is available on the system
- Step 3: Execute $ARTIFACTORY_HOME/bin/artifactory.sh 
- Step 4: Navigate to http://localhost:8082
- Step 5: Use username: admin and password: Password1

Use docker as described at https://www.jfrog.com/confluence/display/JFROG/Installing+Artifactory#InstallingArtifactory-DockerInstallation

    export JFROG_HOME="/Users/timo/swd/packages_project/artifactory-cpp-ce-6.23.13/test"

    docker run --name artifactory -v $JFROG_HOME/artifactory/var/:/var/opt/jfrog/artifactory -d -p 8081:8081 -p 8082:8082 releases-docker.jfrog.io/jfrog/artifactory-cpp-ce:latest


# Jenkins setup

Using docker

https://adamtheautomator.com/jenkins-docker/


docker run --name jenkins -p 8081:8080 -p 50000:50000 jenkins/jenkins:lts
