pipeline {
        agent any
    environment {
        
        dockerImage = ''
    }
    stages{
    
      stage('git checkout'){
      
       steps {
                 
                git branch: 'main', credentialsId: 'gitaccid', url: 'https://github.com/MadhaviAnde/sharks.git'
               
            }
            
                
      }
    
    stage('Building our image') {
            steps {
                
                script {

                    
                    dockerImage = docker.build("sample:$env.BUILD_ID")
                }
            }
        }
      
       
            
            
        
      
}
}
