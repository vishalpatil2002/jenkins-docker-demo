pipeline {
    agent any

    stages {

        stage('Check Docker') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-docker-demo:latest .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker image inspect jenkins-docker-demo:latest'
            }
        }

        stage('List Images') {
            steps {
                sh 'docker images'
            }
        }
    }
}
