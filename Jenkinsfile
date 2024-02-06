pipeline{

    agent any
    
    environment{
        name="jenkins"
    }
    
    parameters{
        string(name: 'username', defaultValue: 'jenkins', description: "IAM")
        booleanParam(select:'isTrue', defaultValue:true, description:"Enter")
    }
    
    stages{
        stage('Run a command'){
            steps{
                sh '''
                pwd
                date
                whoami
                '''
            }
        }
        
        stage('Environmental variable'){
            steps{
                sh 'echo ${BUILD_ID}'
                sh 'echo ${name}'
                // sh 'echo ${username}'
            }
        }
        
        stage('Continue'){
            input{
                message "Should we Continue"
                ok "Yes we should"
            }
            steps{
                echo "Yes continued"
            }
        }
        
        stage('built'){
            steps{
                echo "This is Built Environment"
            }
        }
        
        stage('Test'){
            steps{
                echo "This is Testing Environment"
            }
        }
        
        stage('pre-prod'){
            steps{
                echo "This is Pre Production Environment"
            }
        }   

        stage('prod'){
            steps{
                echo "This is Production Environment"
            }
        }       
    }
}