pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'Building'
          }
        }

        stage('Parallel build') {
          steps {
            echo 'Parallel build'
          }
        }

      }
    }

    stage('copy code') {
      steps {
        git(url: 'https://github.com/amitvpawar/test.git', branch: 'main', poll: true)
        echo 'Copy text files from Git repo'
      }
    }

    stage('') {
      steps {
        sshPublisher()
      }
    }

  }
}