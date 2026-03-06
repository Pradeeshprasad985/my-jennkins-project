pipeline {
    agent any
    tools {
        maven 'Maven-3.9'      // Maven name configured in Jenkins Global Tool Configuration
        jdk 'jdk21'
    }

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'Build Successful'
        }
        failure {
            echo 'Build Failed'
        }
    }
}
