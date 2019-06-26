pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "building"
            }
        }
        stage('Deploy') {
            steps {
                echo "deploying"
                bat "git tag ${BUILD_NUMBER}"
                bat "git push origin --tags"
            }
        }
    }
    post {
        always {
            deleteDir()
        }
    }
}
