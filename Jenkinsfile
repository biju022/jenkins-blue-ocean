pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test step'
          }
        }

        stage('test_parallal') {
          steps {
            echo 'this step is running with parallal to test'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'building'
        sleep 10
      }
    }

  }
}