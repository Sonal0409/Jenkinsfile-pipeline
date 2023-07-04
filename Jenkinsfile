pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        stage('Clone Repo'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        
        stage('Compile Code'){
            steps{
                sh 'mvn compile'
            }
        }
        
        stage('Code Review'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        
        stage('Test code')
        {
            steps{
                sh 'mvn test'
            }
        }
        
          stage('Package code')
        {
            steps{
                sh 'mvn package'
            }
        }
    }
    
    
}
