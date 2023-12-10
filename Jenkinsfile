pipeline {
    agent any
    environment {
        IMAGE_NAME = 'myjenkins-blueocean'
        IMAGE_TAG = '2.426.1-1'
    }
    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Stendhalsynd/jenkins-practice.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        }
    }
}