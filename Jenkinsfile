pipeline{

agent any
 stages{
    stage("maven build"){
     when{
     branch "develop"
     }
     steps{
      sh "mvn clean package"
     }
    }
     stage("sonar analysis"){
     when{
     branch "develop"
     }
      steps{
       echo "perform sonar analysis"
    }
     }
      stage("Deploy to Dev"){
     when{
     branch "develop"
     }
      steps{
       echo "Deploy to Development environment"
    }
      }
  stage("Deploy to QA"){
     when{
     branch "qa"
        }
      steps{
       echo "Deploy to qa environment"
           }
      }
  stage("Deploy to main"){
     when{
     branch "main"
     }
      steps{
       echo "Deploy to master environment"
    }
      }
       
 }
}
