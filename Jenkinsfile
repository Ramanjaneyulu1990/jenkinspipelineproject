pipeline{
    agent any

    stages{

        stage('Pull Repo'){
            steps {
                git 'https://github.com/Ramanjaneyulu1990/jenkinspipelineproject.git'
                
            }
        }

        stage('Build'){
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Publish'){
            steps{
                junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'
            }
            
        }
    }
    
  }
    
}