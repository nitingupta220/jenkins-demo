pipeline{
    agent any
    tools {nodejs "node"}
    stages{
        stage("Get code from Github"){
            steps{
                echo "Checking out code from Github"
                git credentialsId: '1c75fb7c-c157-46c9-8ebc-5175d38d2871', url: 'https://github.com/nitingupta220/jenkins-demo.git'
            }
        }
        stage("Install the dependencies") {
            steps {
                sh "npm install"
            }
        }
        stage("Building the app") {
            steps {
                sh "npm run build"
            }
        }
        stage("Deploying the app") {
            steps {
                sh "npm run deploy"
            }
        }
    }
}