pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        git(url: 'https://github.com/sudhakarbaleboina/helloworld.git', branch: 'master', poll: true)
      }
    }

    stage('build') {
      steps {
        emailext(attachLog: true, subject: '[Jenkins]${currentBuild.fullDisplayName}', body: '\'\'\'<a href="${BUILD_URL}input">click to approve</a>\'\'\'', from: 'baleboinasudhakar@gmail.com', mimeType: 'text/html', to: 'baleboinasudhakar@gmail.com')
      }
    }

  }
}