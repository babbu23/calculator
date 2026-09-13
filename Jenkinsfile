pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }

        stage('Build') {
            steps {
                bat 'python -m py_compile calculator.py app.py'
            }
        }

        stage('Deploy to DEV') {
            steps {
                echo 'Deploying Calculator application to DEV environment...'
            }
        }
    }
}