pipeline {
  agent any
  options {
    buildDiscarder  logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '7', numToKeepStr: '14')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        echo "hello"
      }
     }
    stage('cat README') {
      when {
        branch "fix-*"
      }
      steps {
        sh '''
           cat README.md
	'''
    }
   }
  }
 }
