pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Repository cloned successfully'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t react-vite-app .'
            }
        }

        stage('Complete') {
            steps {
                echo 'CI/CD Pipeline Executed Successfully!'
            }
        }
    }
}
