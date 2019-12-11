pipeline{
	agent any
	tools{
	    maven 'Maven 3.6.1'
	    jdk 'jdk1.1.8.0_181'
	}
	stages{
	stage('build'){
	steps{
	bat 'mvn install'
	}
	post {
	success
	{
	junit 'target/surefire-reports/**/*.xml'
	}
	}
	}
	}
}
