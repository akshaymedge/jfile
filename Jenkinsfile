pipeline {
    agent any
    stages {
        // stage('Example') {
        //     steps {
        //         echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
        //     }
        // }
        stage('Source') {
              git 'https://github.com/chrisparnin/checkbox.io'
          }
        stage('Build') {
            sh 'cd /var/lib/jenkins/workspace/Checkbox/server-side/site
            sh 'npm install'
            sh 'pm2 start server.js'
            sh 'npm test'
            sh 'pm2 stop server.js'
        }
    }
}