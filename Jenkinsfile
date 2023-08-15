pipeline {
  agent any
  tools {
     maven 'M2_HOME'
  }
  environment {
    registry = "gonikai2/devops_pipeline"
    registry = 'dockerhub'
  }
  stages {
    stage('Build'){
      steps {
       sh 'mvn clean'
       sh 'mvn install'
       sh 'mvn package'
      }
    }
     stage('Test'){
      steps {
       sh 'mvn test'
      }
    }
     stage('Deploy'){
      steps {
       echo "Deploy stage"
      }
    }
  }
} 
