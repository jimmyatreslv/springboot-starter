pipeline {
  agent {
    node {
      label 'jdk11'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building..'
          }
        }

        stage('build v1') {
          steps {
            sh 'echo "build v1"'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing..'
          }
        }

        stage('test java') {
          steps {
            sh 'java -version'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}