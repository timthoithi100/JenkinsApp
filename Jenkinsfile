pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "local-test-app"
    }
    stages {
        stage('Build') {
            steps {
                sh "docker build -t ${DOCKER_IMAGE} ."
            }
        }
        stage('Test') {
            steps {
                sh "docker run --rm ${DOCKER_IMAGE}"
            }
        }
    }
}
