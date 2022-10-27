pipeline {
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/Qwerty5932/test.git"
            }
        }
        stage("Build"){
            steps {
                dir("aa"){
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                dir("simple-java-maven-app"){
                    sh "mvn test"
                }
            }
        }
    }
}