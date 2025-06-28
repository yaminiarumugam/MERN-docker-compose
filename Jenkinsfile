pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'compose', url: 'https://github.com/yaminiarumugam/MERN-docker-compose.git'
            }
        }

        stage('Docker Compose Build & Up') {
            steps {
                sh 'docker-compose down || true'
                sh 'docker-compose up -d --build'
            }
        }
    }
}
