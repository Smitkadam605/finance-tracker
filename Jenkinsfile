
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Finance Tracker source code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn -B clean package'
            }
        }

        stage('Selenium Tests') {
            steps {
                echo 'Selenium test stage will run after build configuration'
            }
        }
    }

    post {
        success {
            echo 'Finance Tracker pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}

