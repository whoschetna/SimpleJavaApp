pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/whoschetna/SimpleJavaApp.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    // Make sure npm is available on the agent
                    sh 'npm install'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Here you can add commands to deploy your app
                    // Example: Start a simple local server
                    sh 'npm start'
                }
            }
        }
    }

    post {
        always {
            echo 'Cleaning up'
        }
    }
}
