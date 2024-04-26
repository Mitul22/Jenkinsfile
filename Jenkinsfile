pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "Documents/Jenkinsfile"
        TESTING_ENVIRONMENT = "Testing Environment"
        PRODUCTION_ENVIRONMENT = "Mitul Tandon"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                script {
                    echo "Waiting for manual approval..."
                    sleep 10
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the code to the production environment using the environment variable specifying the environment name: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
