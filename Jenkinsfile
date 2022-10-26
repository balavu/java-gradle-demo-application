pipeline {
    
    agent any
    
    stages {
        
		stage('Checkout Code') {
			steps {
				checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dinushchathurya/java-gradle-demo-application.git']]])
			}
		}
		
	    stage('Build') {
            steps {
                sh './gradlew build'
            }
	    }
	    
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        
        stage('Check') {
            steps {
                sh './gradlew check'
            }
        }      
		
	}
}
