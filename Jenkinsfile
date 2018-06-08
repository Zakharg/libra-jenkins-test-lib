pipeline {
    agent any 

    stages {
        stage ('Compile stage') {
            steps {
	            withMaven(maven : 'Maven 3.5.0', globalMavenSettingsConfig: "12901f1e-1275-4898-a045-d4eed3f5303a") {
	                sh 'mvn clean install'
            	}
            }
        }
        
        stage ('Deployment Stage') {
            steps {
	   			withMaven(maven : 'Maven 3.5.0', globalMavenSettingsConfig: "12901f1e-1275-4898-a045-d4eed3f5303a") {
	            	sh 'mvn deploy'
            	}
            }
        }
    }

}