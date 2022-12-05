pipeline {
  agent any
  stages {
    stage('clean') {
      agent any
      steps {
        echo 'clean step'
      }
    }

    stage('build_master') {
      parallel {
        stage('build_master') {
          agent {
            node {
              label 'master'
            }

          }
          steps {
            sleep 5
          }
        }

        stage('') {
          agent {
            node {
              label 'alg_slave'
            }

          }
          steps {
            echo 'alg slave'
          }
        }

      }
    }

  }
}