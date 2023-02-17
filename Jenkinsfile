pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o CS687 CS687.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './CS68'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployed successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
