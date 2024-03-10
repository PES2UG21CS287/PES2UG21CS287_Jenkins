pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS256-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Display') {
      steps {
        echo "display"
      }
    }
  }
  post {
failure {
  error 'Pipeline Failed'
}
  }
}
