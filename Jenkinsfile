pipeline {
  agent any

  environment {
    IMAGE_NAME = "my-fullstack-app"
  }

  stages {
    stage('Checkout Code') {
      steps {
        git 'https://github.com/huuhai28/fullstack-devops.git'
      }
    }

    stage('Build Docker Images') {
      steps {
        sh 'docker-compose build'
      }
    }

    stage('Run Containers') {
      steps {
        sh 'docker-compose up -d'
      }
    }

    stage('Verify Running Services') {
      steps {
        sh 'docker ps'
      }
    }
  }
}
