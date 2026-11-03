pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t java-add-numbers-image .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run java-add-numbers-image'
            }
        }
    }

    post {
        always {
            sh 'docker rmi java-add-numbers-image'
        }
    }
}
