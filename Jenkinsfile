pipeline {
    agent any
    
    stages {
        stage('Building') {
            steps {
                sh 'docker build -t clockbox .'

            }
        }

        stage('Testing') {
            steps {
                sh 'python3 -m unittest'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d clockbox'
            }
        }

    }
}
