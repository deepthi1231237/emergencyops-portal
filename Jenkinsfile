pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t emergencyops-portal .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8082:80 emergencyops-portal'
            }
        }
    }
}