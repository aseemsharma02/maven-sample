pipeline { 
    agent any 
    tools {
        maven 'M2_HOME'
          }
    stages {
        stage('Checkout') {
        steps {
		git 'https://github.com/devopscbabu/maven-sample.git'
               }
            }
	stage('Validate') {
        steps {
		sh 'mvn clean validate'
               }
            }	    
        stage('Build') { 
            steps { 
                sh 'mvn clean compile'
            }
	    }
	  stage('package your app') { 
            steps { 
                sh 'mvn clean package'
            }
        }  
	}
}
