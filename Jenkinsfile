pipeline {
    agent any

    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM',
        //             // branches: [[name: '*/main']],
        //             userRemoteConfigs: [[url: 'https://github.com/Sree-Harsha-PS/PES2UG21CS356_Jenkins.git']]])
        //     }
        // }
        stage('Build') {
            steps {
                build 'PES2UG21CS356-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
