pipeline {
  agent none

  stages {
    
    stage('Back-end') {
      agent {
        docker { image 'maven:3.8.1-adoptopenjdk-11' }
      }
      steps {
        sh 'mvn --version'
        sh 'echo "Back-end build or tests here..."'
      }
    }

    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
        sh 'echo "Front-end build or npm install here..."'
      }
    }

    stage('Database') {
      agent {
        docker { image 'mysql:5.7' }
      }
      steps {
        sh 'echo "Simulate DB setup or connection test..."'
      }
    }

  }
}
