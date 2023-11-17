pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Script') {
            steps {
                sh 'bash script.sh'
            }
        }
    }

    post {
        success {
            echo 'The workflow completed successfully. Ready for deployment!'
        }
        failure {
            echo 'The workflow has failed. Check the logs for more details.'
        }
    }
}
