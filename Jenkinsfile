pipeline {
  agent any
  stages {
    stage('Local Setup') {
      parallel {
        stage('Local Setup') {
          steps {
            sleep 3
          }
        }
        stage('Check Endevor Package Status') {
          steps {
            sleep 6
          }
        }
      }
    }
    stage('Build All') {
      parallel {
        stage('Build Windows App') {
          steps {
            sleep 4
          }
        }
        stage('Build Linux App') {
          steps {
            sleep 3
          }
        }
        stage('Build Mainframe Cobol Code') {
          steps {
            sh 'gulp build'
          }
        }
        stage('Build iOS Apps') {
          steps {
            sleep 31
          }
        }
        stage('Build Android App') {
          steps {
            sleep 41
          }
        }
      }
    }
    stage('Test Apps') {
      parallel {
        stage('Test Apps') {
          steps {
            sleep 1
          }
        }
        stage('Unit Tests') {
          steps {
            sleep 3
          }
        }
      }
    }
    stage('Deploy to QA') {
      parallel {
        stage('Deploy to QA') {
          steps {
            sleep 1
          }
        }
        stage('Copy Load Libs') {
          steps {
            sleep 12
          }
        }
        stage('Refresh CICS') {
          steps {
            sleep 12
          }
        }
      }
    }
    stage('SIT Testing') {
      parallel {
        stage('SIT Testing') {
          steps {
            sleep 12
          }
        }
        stage('Mainframe JCL Testing') {
          steps {
            sleep 12
          }
        }
        stage('Mainframe WS Testing') {
          steps {
            sleep 12
          }
        }
        stage('Mainframe CICS Testing') {
          steps {
            sleep 12
          }
        }
        stage('iOS Testing') {
          steps {
            sleep 12
          }
        }
      }
    }
  }
}