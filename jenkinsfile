pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven'
    }

    stages {
        stage('Git Check-Out') {
            steps {
                git branch: 'main', url: 'https://github.com/chhagan72/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                sh " mvn clean compile"
            }
        }
        stage('Build') {
            steps {
                sh " mvn clean package -DskipTests=true"
            }
        }
    }
}
