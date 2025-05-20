pipeline{
  agent any
 triggers {
        githubPush()
    } 
  stages {
    stage("build") {
      steps {
          // sh 'npm install'
          // sh 'npm build'
          echo 'building the app...'
      }
    }
    stage('Hello') {
       steps {
          echo 'Triggered by GitHub!'
            }
        }
    stage("test") {
      when{
          expression{
          BRANCH_NAME == 'dev' || BRANCH_NAME == 'main'
          }
      }
      steps {
          echo 'testing the app...'
      }
    }
    stage("deploy") {
      steps {
          echo 'deploying the app...'
      }
    }
  }
}
