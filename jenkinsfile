pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
               git 'https://github.com/pranathi1319-sudo/git_dir_demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t web-image-a .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8091:80 web-image-app'
            }
        }
    }
}