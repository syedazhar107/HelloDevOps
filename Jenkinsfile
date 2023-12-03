pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the Git repository
                git 'https://github.com/yourusername/HelloDevOps.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }
        
        // Add more stages for testing, deployment, etc.
    }
    
    post {
        success {
            echo 'Build successful! Deploy your application.'
            // Add deployment steps here
        }
        failure {
            echo 'Build failed! Notify the team.'
            // Add notification or rollback steps here
        }
    }
}

