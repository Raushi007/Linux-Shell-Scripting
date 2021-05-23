pipeline{
    agent {
        label "agent"
    }
    environment{
        myvar="outer block"
    }
    stages{
            stage('checkout'){
                steps{
                git credentialsId: 'GitJenkins', url: 'https://github.com/Raushi007/Linux-Shell-Scripting.git'
            }
            }
            stage('build'){
                steps{
                sh 'sh arrays.sh'
                sleep 10
                }
            }
            stage('post task'){
                steps{
                sh 'echo email'
                }
            }
            stage('printing enviroment varaiable'){
                environment{
                    myvar="inner block"
                }
                steps{
                    sh 'echo "this is my varaiable $myvar"'
                }
            }
    }
}

