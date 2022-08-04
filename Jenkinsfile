pipeline {
  agent any

  environment {
    imageName = "myapp"
    registryCredentials = "nexusid1"
    registry = "35.172.201.214:8083"
    dockerImage = ''
  }
  options {
    buildDiscarder logRotator(daysToKeepStr: '5', numToKeepStr: '7')
  }
  stages {
    stage('Build') {
      steps {
        sh script: 'mvn -f MyAwesomeApp/pom.xml clean package'
      }
    }

  }
}

