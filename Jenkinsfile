pipeline {
  agent {
    node {
      label 'slave2'
    }

  }
  stages {
    stage('Unit') {
      parallel {
        stage('BattUDiag') {
          steps {
            echo 'Static Analysis'
            echo 'Unit Test'
          }
        }
        stage('SteerWhlTq') {
          steps {
            echo 'Static Analysis'
            echo 'Unit Test'
          }
        }
        stage('Assist') {
          steps {
            echo 'Static Analysis'
            echo 'Unit Test'
          }
        }
      }
    }
    stage('Build') {
      steps {
        echo 'Build'
      }
    }
    stage('Integration') {
      parallel {
        stage('Static Analysis') {
          steps {
            echo 'Static Analysis'
          }
        }
        stage('Interface Test') {
          steps {
            echo 'Inteface Test'
          }
        }
        stage('Resource Usage') {
          steps {
            echo 'Resource Usage'
          }
        }
      }
    }
    stage('Qualification') {
      parallel {
        stage('Qualification') {
          steps {
            echo 'Communication'
          }
        }
        stage('Communication') {
          steps {
            echo 'Communcation Test'
          }
        }
        stage('Control Function') {
          steps {
            echo 'Control Function'
          }
        }
        stage('Diagnostic') {
          steps {
            echo 'Diagnostic'
          }
        }
      }
    }
    stage('Documentation') {
      parallel {
        stage('Release Note') {
          steps {
            echo 'Release Note'
          }
        }
        stage('Test Result upload') {
          steps {
            echo 'Test Result Upload'
          }
        }
      }
    }
    stage('Release') {
      steps {
        echo 'Deploy'
      }
    }
  }
}