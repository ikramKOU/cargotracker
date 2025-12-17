pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Clone') {
            steps {
                
                git branch: 'main', url: 'https://github.com/eclipse-ee4j/cargotracker.git'
            }
        }

        stage('Build & test') {
            steps {
                bat 'mvn clean verify'
            }
        }

       

       
    }

    
}
