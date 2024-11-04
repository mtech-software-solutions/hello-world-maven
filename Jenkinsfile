pipeline {
    agent any
    tools {
        maven "M3"
    }
    stages {
        stage('Repo Setup') {
            steps {
                git branch: 'main', url: 'https://github.com/TheEarlOfGray/first-jenkins.git'
            }
        }
        stage('Build') {
            steps {
                sh 'bash setup.sh'
                sh 'ls'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn run'
            }
        }
    }
}
