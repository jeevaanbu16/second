pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                node('nodejs') {
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
        stage('Push') {
            steps {
                node('nodejs') {
                    sh 'npm run deploy'
                }
            }
        }
    }
}
