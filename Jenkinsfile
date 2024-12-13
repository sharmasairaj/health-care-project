pipeline {
    agent any

    tools {
        jdk 'JDK23'     
        maven 'Maven3'   
    }
    stages {
        stage('checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/sharmasairaj/health-care-project.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn clean compile install'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
