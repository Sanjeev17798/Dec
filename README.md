# Dec

pipeline {
    agent any 
    stages{
        stage("code"){
        { 
          steps{
            echo "Cloning the code"
            git url:"https://xyz",branch: "main"
          }
        }
        }
        stage("build"){
          steps{
           echo "bulding"
           sh "any shell command write here in same formate after sh there should space and write the command into double quotes"
          }
        }
        stage("deploy"){
          steps{
            echo "deploying the code"
          }
        }       
  }
}
