pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'PrintingMessage'
      }
    }

    stage('step2') {
      agent {
        docker {
          image 'node:lts-alpine'
          args '-p 3000:3000'
        }

      }
      steps {
        sh 'npm install'
      }
    }

  }
}