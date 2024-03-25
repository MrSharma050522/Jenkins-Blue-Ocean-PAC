pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo "This is Hello World From Build Stage"
pwd
date'''
      }
    }

    stage('Test Stage') {
      parallel {
        stage('Test Stage') {
          steps {
            sh 'echo "Test Step"'
          }
        }

        stage('Test Parallell') {
          steps {
            sh 'echo "Running Test Stage Parallely"'
            echo 'Test Parallel'
          }
        }

      }
    }

    stage('Deploy In Test') {
      steps {
        echo 'Deploying In Test'
      }
    }

  }
}