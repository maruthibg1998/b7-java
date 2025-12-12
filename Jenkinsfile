pipeline {
    agent any
    
    environment {
        git_branch = 'main'
        git_url = 'https://github.com/maruthibg1998/b7-java.git'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: "${git_branch}", url: "${git_url}"
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Build Project') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
