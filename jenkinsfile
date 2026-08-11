pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Package') {
            steps {
                sh 'echo "Jenkins Pipeline Successful" > build.txt'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'build.txt', fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
