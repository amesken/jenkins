[![](https://badge.imagelayers.io/amesken/jenkins:latest.svg)](https://imagelayers.io/?images=amesken/jenkins:latest 'Get your own badge on imagelayers.io')

# Jenkins

Run [Jenkins](https://jenkins-ci.org/) inside a Docker container.

## Volumes
Jenkins home directory is exported as data volume:

    <USER_HOME>/docker/data/jenkins

## Ports
The service is exposed through port `8080`.

## Example
To run jenkins do:

	docker run -p 18080:8080 amesken/jenkins

Now point your browser to http://192.168.99.100:18080/

There is no admin user needed.

## Jenkins config and jobs
This image will configure jenkins to work with a complete Continuous Delivery tool stack which can be obtained from [docker](https://hub.docker.com/r/amesken/cd-tool-stack/) or [github](https://github.com/amesken/cd-tool-stack).
The jenkins jobs and configuration are based on [this blog article](https://blog.codecentric.de/en/2015/10/continuous-integration-platform-using-docker-container-jenkins-sonarqube-nexus-gitlab) by Marcel Birkner.