pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3003:3003'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deliver') {
            steps {
                sh 'npm start'
            }
        }
    }
}
