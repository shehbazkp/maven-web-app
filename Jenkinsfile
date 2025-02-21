pipeline {
    agent any
    
    tools{
        maven "maven"
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/shehbazkp/maven-web-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Execute Playbook') {
            steps {
                sh 'ansible-playbook task.yml'
            }
        }
    }
}
