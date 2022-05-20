@Library('newlibrary')_
node('built-in') 
{
    stage('ContinuousDownload_Master') 
    {
        cicd.newGit("https://github.com/krishnain/maven7.git") 
    }
    stage('ContinuousBuild_Master') 
    {
         cicd.newMaven()
    }
    stage('ContinuousDeployment_Master')
    {
         cicd.newDeploy("172.31.27.136","testapp")
    }
    stage('ContinuousTesting_Master')
    {
        
         cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                    cicd.runSelenium("/home/ubuntu/.jenkins/workspace/DeclarativePipelinewithSharedLibrarires")
    }
    stage('ContinuousDelivery_Master')
    {
        cicd.newDeploy("172.31.28.209","prodapp")
        
    }
    
    
    
    
    
    
    
    

    
    
    
}

