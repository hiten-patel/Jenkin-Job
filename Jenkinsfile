pipeline {
    agent any
    stages {
        // stage("Clean Up"){
        //     steps {
        //         deleteDir() 
        //     }
        // }
        // stage("Clone repo"){
        //     steps {
        //         sh "git clone https://github.com/hiten-patel/Jenkin-Job.git"
        //     }
        // }
        stage("Build"){
            steps {
                dir("MavenHelloWorld") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                 dir("MavenHelloWorld") {
                    sh "mvn test"
                }
            }
        }
        stage("Complete"){
            step {
                echo "Job Commpleted"
            }
        }
    }
}