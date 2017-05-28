pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build(job: 'build-openshift', propagate: true)
      }
    }
    stage('Deploy') {
      steps {
        bat 'java -jar target'
      }
    }
  }
}