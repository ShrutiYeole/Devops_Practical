pipeline {
    agent any 
    stages {
        stage('Hello') {
            steps {
                echo 'Hello Kaustubh' 
            }
        }
        stage ('code phase'){
            steps{
                input('Do you want to continue?')
            }
        }
        stage ('testing phase'){
             parallel{
                    stage ('parallel one'){
                        steps{
                            echo 'running 1st parallel stage'
                            input('Do you want to continue on second stage?')
                        }
                    }
                     stage ('parallel two'){
                        steps{
                            echo 'running 2nd parallel stage'
                        }
                    }
             }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests again' 
            }
        }
    }
}
