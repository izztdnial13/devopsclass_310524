pipeline {
    agent any
    triggers {
        pollSCM '*/5 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                sh '''
                sudo apt update
                sudo apt upgrade -y
                sudo apt-get install python3 -y
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                python3 -V
                '''
            }
        }
        stage('Deliver') {
            steps {
                sh '''
                echo "Ready to deliver"
                '''
            }
        }
    }
}
