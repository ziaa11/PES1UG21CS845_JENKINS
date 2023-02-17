pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
          sh 'g++ -o output main/sample.cpp'
          build 'PES1UG21CS845-1'
          echo 'Build stage successful'
        }
      }
      stage('Test') {
        steps {
        sh './output'
        }
      }
      stage('Deploy') {
        steps {
          echo 'Application is deployed'
        }
      }
    }
    post {
      failure{
        echo 'Pipeline failed'
      }
    }
}
