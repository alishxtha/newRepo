pipeline {
    agent any

    stages {
        stage('Code Fetch') {
            steps {
                echo 'Code fetch from gitHub'
                git url: 'https://github.com/alishxtha/newRepo.git' , branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t my-new-website . '
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying on Container'
                sh 'docker run -d -p 80:80 my-new-website  '
                
            }
        }
    }
}
