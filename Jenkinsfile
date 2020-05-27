pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Uploading html file to s3..."'

        withAWS(region:'us-west-2', credentials:'aws-static') {
          s3Upload(file:'index.html', bucket:'project3-s3-static')
        }

      }
    }
  }
}

