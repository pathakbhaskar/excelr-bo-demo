pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/pathakbhaskar/excelr-bo-demo.git', branch: 'main')
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}