pipeline {
	agent {  label 'linux-node' }
	stages {
		stage('---clean---'){
			tools {
				maven 'MAVEN-3.8.6'
			}
			steps {
				
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'MAVEN 3.5.3'
			}
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			
			steps {
				
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was building successfully'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
