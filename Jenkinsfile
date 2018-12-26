  node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){ 
      sh 'mvn package'
   }
   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/T8CCN0CG1/', channel: 'jenk-slack', color: 'good', message: 'Hello All !!', teamDomain: 'ibm-gts-cic-india', tokenCredentialId: 'int-tok'
   }
}
