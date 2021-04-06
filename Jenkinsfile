pipeline {
  agent any 
  environment{
    NEW_VERSION='1.3.0'
    SERVER_CREDENTIALS = credentials('123035ea-b4c2-4ea1-9eb7-25ac3db30391')
  }
  stages {
    stage("build"){
    steps{
          echo "building the application"
      echo "building version ${NEW_VERSION}"
    }}
    stage("test"){
    steps{
           echo "testing the application"
    }}
    stage("deploy"){
     steps{
           echo "deploying the application"
       echo "deploying with ${SERVER_CREDENTIALS}"
       sh "${SERVER_CREDENTIALS}"
    }}
    post{
      always {
        //
      }
      success {
        //
      }
      failure{
        //
      }
    }
  }}

