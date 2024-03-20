pipeline {
    agent {
        label 'first'
    }
    tools {
        maven 'maven'
    }

    stages {
        
        stage('Python') {
            steps {
                git branch: 'python', url: 'https://github.com/Lalit280/mar-20.git'
                sh "python3 main.py"
            }
        }
        stage('Shell') {
            steps {
                git branch: 'shellscript', url: 'https://github.com/Lalit280/mar-20.git'
                sh "bash factorial.sh"
            }
        }
        stage('maven') {
            steps {
                git branch: 'maven', url: 'https://github.com/Lalit280/mar-20.git'
                sh "mvn clean install"
            }
        }
    }
}
