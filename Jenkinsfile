/*node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test'){
		echo "Integration Test"
	}
}
*/

//Declarative

pipeline {
	agent { docker { image 'maven:3.6.3'} }
	stages{ 
		stage('Build') {
			steps {
				echo "Build with Maven"
				sh 'mvn --version' 
			}
		}
		stage("Test") {
			steps {
				echo "Test"
			}
		}

		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	
	post {
		always {
			echo "I run always ! "
		}
		success{
			echo "I run when successful !! "
		}
		failure {
			echo "I run when I fail !!!"
		}

	}
}