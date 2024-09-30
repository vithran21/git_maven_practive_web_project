pipeline {
    agent any
    tools {
        maven "maven"
    }
    stages {
        stage ('pull src from git') {
            steps {
              git 'https://github.com/vithran21/git_maven_practive_web_project.git'
            }
        }
        stage ('mvn version check') {
            steps {
                sh 'mvn --version'
            }
        }
        stage ('maven build steps') {
            steps {
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
    }
    post {
        success {
            echo "Build is successfully generated"
        }
        failure {
            echo "Build is failing, check details"
        }
    }
}
