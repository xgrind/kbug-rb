pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependences'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running reggression tests'
            }
        }
        stage('UAT') {
            steps {
                echo 'Wait for User Acceptance'
                input(message: 'Go to production?', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'WebApp is Ready'
            }
        }
    }
}