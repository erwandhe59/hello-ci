pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying...'
                }
            }
        }
    }
    post {
        success {
            script {
                echo 'Build succeeded :) !'
            }
        }
        failure {
            script {
                echo 'Build failed!'
            }
        }
    }
}