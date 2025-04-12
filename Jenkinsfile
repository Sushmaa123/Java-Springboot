pipeline {
    agent {label 'slave-1'}
    tools {
      maven 'maven'
    }
    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/Sushmaa123/Java-Springboot.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn package'
            }
        }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
post {
        always {
            emailext(
                to: 'sushmaananda999@gmail.com',
                subject: 'Build ${BUILD_NUMBER} - ${BUILD_STATUS}',
                body: 'The build has completed with status: ${BUILD_STATUS}',
                attachLog: true
            )
        }
    }

}

       
