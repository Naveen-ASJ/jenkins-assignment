pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Naveen-ASJ/jenkins-assignment.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sample-webapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 --name webapp sample-webapp'
            }
        }
    }
}
