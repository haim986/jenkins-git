pipeline {

    agent { label 'master' }
  
  
    options {
  
      disableConcurrentBuilds()
      timeout(time: 10, unit: 'MINUTES')
      buildDiscarder(logRotator(numToKeepStr: '10'))
  
    } // options
  // parameters
  
    
  
    stages {
   
      stage("Deliver for master") { 
          when {
                  branch 'master'
              }
        steps {
          script {
            //enable remote triggers
            properties([pipelineTriggers([pollSCM('* * * * *')])])
            sh 'date'
            
  
  
          }
        }
      }
      
    }
}
