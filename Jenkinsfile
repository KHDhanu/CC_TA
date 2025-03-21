pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/KHDhanu/CC_TA.git'
            }
        }
        stage('Build C++') {
            steps {
                sh 'g+ hello.cpp -o output'
                echo 'Build completed successfully'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!!'
        }
    }
}
