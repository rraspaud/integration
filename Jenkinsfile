pipeline {
    agent any

    stages {
         stage('Checkout') {
            steps {
                git 'https://github.com/rraspaud/integration.git'
            }
        }
        stage('Build') {
            steps {
                dir('maven-demo-1') {
                    bat label: '', script: 'mvn install'
                }
            }
        }
        stage('Test') {
            steps {
                dir('maven-demo-1') {
                    bat label: '', script: 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
