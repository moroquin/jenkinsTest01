pipeline {
  agent any
  tools {
    nodejs 'node17.6'
  }

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

  stages {
    stage('Install dependencies') {
      steps {
        sh 'cd jenkins-tests && npm i'
      }
    }
    stage('Run tests') {
      steps {
        sh 'cd jenkins-tests && npm t'
      }
    }
  }
}
