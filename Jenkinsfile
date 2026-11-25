pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting source code from GitHub'
                checkout scm
            }
        }

        stage('Run Python Program') {
            steps {
                echo 'Executing Python program'
                sh 'python3 PDCJenkinsLab.py'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }

        failure {
            echo 'BUILD FAILED!'
        }
    }
}
