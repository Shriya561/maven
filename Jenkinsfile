pipeline {
    agent any

    stages {

        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }

        stage('Package JAR') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Install') {
            steps {
                sh 'mvn install'
            }
        }

    }

    post {
        failure {
            echo 'Build failed'
        }
        success {
            echo 'Build successful'
        }
    }
}