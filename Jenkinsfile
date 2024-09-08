pipeline {
    agent {
        docker {
            image 'node:14'
        }
    }
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('my-node-app')
                }
            }
        }
        stage('Test') {
            steps {
                sh 'npm install'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps here
            }
        }
    }
}
