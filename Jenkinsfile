pipeline {
  agent any
  stages {
    stage('maven Test') { 
      steps {
        sh 'mvn clean test'
      }
    }
     stage('Deploy CloudHub') { 
     steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=3.9.0 -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}' 
      }
    }
    }
    }
