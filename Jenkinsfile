pipeline {
  agent any
  stages {
    stage('Verify Branch'){
      steps {
        echo "GIT_BRANCH"
      }
    }
    stage('Docker build'){
       steps{
        dir('azure-vote') {
        sh 'docker images -a'
        sh 'docker build -t jenkins-pipeline .'
        sh 'docker images -a'
        sh 'cd ..'
        }
        
        }
    }
      
  }
}
