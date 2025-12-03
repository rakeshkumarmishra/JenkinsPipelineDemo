
pipeline {
    agent any

    environment {
        BROWSERSTACK_USERNAME = rakmis_yixdpb
        BROWSERSTACK_ACCESS_KEY = JEcpG4UVC6Uq5oAFSHVC
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rakeshkumarmishra/JenkinsPipelineDemo.git'
            }
        }

        stage('Build & Test') {
            steps {
                sh 'mvn clean test -Dbrowserstack=true'
            }
        }

        stage('Archive Results') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
