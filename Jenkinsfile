pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
              steps {
                  withAWS(region:'eu-west-2',credentials:'ACredentials') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkweb')
                  }
              }         
         
     }
}
}
