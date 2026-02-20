pipeline {
  agent any
  tools {
    maven 'M2_HOME'
  }
  stages {
    stage('Code Build') {
      steps {
        sh 'mvn install -Dmaven.test.skip=true -f student-management/pom.xml'
      }
    }
  }
  post {
    always { echo "======always======" }
    success { echo "=====pipeline executed successfully =====" }
    failure { echo "======pipeline execution failed======" }
  }
}