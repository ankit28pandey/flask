pipeline {
    agent any

    stages {
        stage('Get Code') {
            steps {
                git branch: 'main', url: 'https://github.com/ankit28pandey/flask.git'
            }
        }
        stage('docker build') {
            steps {
                sh 'docker build -t flask-rest-api .'

            }
        }
        stage('docker run'){
            steps {
                sh 'docker run -d -p 7000:7000 flask-rest-api'
            }
        }
    }
}
