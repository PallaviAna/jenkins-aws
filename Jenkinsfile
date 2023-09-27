pipeline{
    agent any

    tools{
        maven "maven"  //which tools we are using in our project that
        //we can mention in tools script/block
        //docker "docker"
    }


    environment{
        VERSION_NAME="1.34"
    }

    stages{

        stage("compile"){
            // when{
            //     expression{
            //         //for running below stage we can give here condition 
            //         //as well. For that we can use environment varibale or
            //         //jenkins global varibale // link for this is : 
            //         //http://16.171.241.62:8080/env-vars.html/
            //     }
            // }
            steps{
                sh 'javac Test.java'
                sh 'echo "${VERSION_NAME}"'
            }

        }

        stage("run"){
            steps{
                sh 'java Test'
            }

        }


    }

    post{
        always{
            sh 'echo "always"'
        }

        success{
            sh 'echo "success"'
        }

        failure{
            sh 'echo "failure"'
        }
    }
}