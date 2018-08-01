pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/SinhaSurajit', branch: 'prgxlabrepo')
      }
    }
    stage('Testing') {
      parallel {
        stage('Testing') {
          steps {
            sh 'echo "Running unit test"'
          }
        }
        stage('Functional Testing') {
          steps {
            sh 'echo "Functional test"'
          }
        }
      }
    }
    stage('Deploy to QA') {
      steps {
        sh 'echo "Deploy to QA"'
      }
    }
    stage('System Testing') {
      steps {
        sh 'echo "System Testing"'
      }
    }
    stage('Deploy to PROD') {
      steps {
        sh 'echo "Deploy to PROD"'
      }
    }
  }
}