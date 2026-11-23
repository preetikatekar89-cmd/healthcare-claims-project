pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Downloading code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Healthcare Application'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                echo 'Application test successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to Apache'
                sh 'cp index.html /var/www/html/index.html'
            }
        }
    }
}
