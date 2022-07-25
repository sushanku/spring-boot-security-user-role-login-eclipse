pipeline {
  agent any
  stages {  
    stage('Build') {
      steps {
          sh "./gradlew clean build"
      }
    }
    
    stage ('Sonarqube Analysis') {
      steps {
        withSonarQubeEnv('springboot-login-gradle') {
          sh "./gradlew sonarqube"
        }
      }
    }
  }
}