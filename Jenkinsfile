pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials: 'aws-static', region: 'us-east-1') {
          s3Upload(bucket: 'project3-jenkins-lquinonez', pathStyleAccessEnabled: true, payloadSigningEnabled: true, file: 'index.html')
        }

      }
    }
  }
}