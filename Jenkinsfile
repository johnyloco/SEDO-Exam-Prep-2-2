pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Restore Dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build the Project') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Test the Project') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
