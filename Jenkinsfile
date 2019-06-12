pipeline {
  agent any
  stages {
    stage('Test') {
      agent { label 'nodejs-app' }
      steps {
        container('nodejs') {
          echo 'Hello World!'   
          sh 'java -version'
        }
        steps {
           error 'fake error to force failure in test stage/gate'
        }
      }
    }
  }
