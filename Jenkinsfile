pipeline {

	agent any
	
	tools {
		maven "MY_MAVEN"
		jdk "MY_JAVA"

	}
	
	stages {
		stage('Initialise') {
			steps {
				echo "PATH = ${M2_HOME}/bin:${PATH}"
				echo "M2_HOME = /opt/maven"
			}
		}
		stage('Build') {
			steps {
				dir("/var/lib/jenkins/workspace/JavaBuildPipeline/my-app"){
					sh 'mvn -B -DskipTests clean package'
				}
			}
		}
	}
}
			

	
