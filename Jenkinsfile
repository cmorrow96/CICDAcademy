#!groovy?
 
pipeline {
    // agent any
    agent {
        docker { image 'node:18' }
    }

    stages {
        stage('Pull Request') {
            when {
                anyOf {
                    changeRequest()
                }
            }
            steps {
                echo "PR"
            }
        stage('Build') {
            steps {
                echo 'Building..'
                // dir('api') {
                //     script {
                //         docker.build("test-api:${env.BUILD_ID}")
                //     }
                // }
            }
        }


        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
