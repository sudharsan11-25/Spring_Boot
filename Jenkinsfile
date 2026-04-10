pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'Maven3'
    }

    environment {
        JAVA_HOME = tool 'JDK21'
        PATH = "${env.JAVA_HOME}\\bin;${env.PATH}"
    }

    stages {

        stage('Build') {
            steps {
                bat 'echo JAVA_HOME=%JAVA_HOME%'
                bat 'java -version'
                bat 'mvn clean install'
            }
        }

        stage('Test Run') {
            steps {
                bat 'mvn test'
            }
        }
    }
}