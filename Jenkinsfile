pipeline {
    agent any
    
    tools {
        jdk 'jdk11'
        maven 'maven2'
    }
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Slybss/BoardgameListingWebApp.git'
            }
        }
        
        stage('compile') {
            steps {
                sh "mvn compile"
            }
        }
        
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
    
        stage('install') {
            steps {
                sh "mvn install"
            }
        }
    }
}
