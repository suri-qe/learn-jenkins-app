pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "Without docker"'
            }
        }
        
        stage('w/ docker') {
            agent {
                docker {
                    image 'node:20-alpine'
                }
            }
            steps {
                sh '''
                    echo "With docker"
                    npm --version
                '''
            }
        }
    }
}