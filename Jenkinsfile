pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t my-website .'
            }
        }

        stage('Docker Run') {
            steps {
                bat 'docker run -d -p 8081:80 --name my-website-container my-website'
            }
        }
    }
}
