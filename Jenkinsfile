pipeline {
  agent none
  stages {
    stage('test') {
      steps {
        sh '''stage(\'Test\') {
            steps {
                sh \'mvn test\'
            }
            post {
                always {
                    junit \'target/surefire-reports/*.xml\'
                }
            }
        }'''
        }
      }
    }
  }