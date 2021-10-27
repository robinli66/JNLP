pipeline {
  agent {
    node {
      label 'docker-jenkins'
    }
    
  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'git@github.com:practicaljenkins/python-project.git', branch: 'master', credentialsId: '597e1eb7-0133-469d-90f4-cf78e915c456')
      }
    }
    stage('build') {
      steps {
        sh 'python *test.py'
      }
    }
  }
}
