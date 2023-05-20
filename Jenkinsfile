pipeline {
    agent any
    stages {
        stage('git repo clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Pranathi99/TestProject-Frontend.git'
            }
        }
        // stage('clean') {
        //     steps {
        //         sh "mvn clean"
        //     }
        // }
        // stage('package') {
        //     steps {
        //         sh "mvn package"
        //     }
        // }
        // stage('docker build') {
        //     steps {
        //         sh "docker build -t employee-management ."
        //     }
        // }
        // stage('docker compose build') {
        //      steps {
        //          sh "docker build -t angular-my-movie-plan:1.0 -f Dockerfile ."
        //      }
        // }

        stage('docker compose start') {
             steps {
                 sh "docker run -d -p 4200:80 angular-my-movie-plan:1.0"
             }
        }
    }
}
