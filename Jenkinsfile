pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/VIVEKNAIDU0701/fastapi-hello.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run App') {
            steps {
                bat 'python -m uvicorn app.main:app'
            }
        }
    }
}