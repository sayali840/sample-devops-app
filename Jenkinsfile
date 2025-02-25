pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "sample-devops-app"
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/sample-devops-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 $DOCKER_IMAGE'
            }
        }
    }
}
