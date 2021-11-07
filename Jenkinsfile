pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "rm -rf /var/www/testpwa"
                sh "cp -r ${WORKSPACE}/build/ /var/www/testpwa/"
            }
        }
    }
}