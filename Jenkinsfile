pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/vignesh-lnp/docker-jenkins-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t docker-jenkins-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
<<<<<<< HEAD
                    docker stop docker-jenkins-demo
                    docker rm docker-jenkins-demo
                    docker run -d --name docker-jenkins-demo -p 4000:3000 docker-jenkins-demo
=======
                    docker stop docker-jenkins-demo || true
                    docker rm docker-jenkins-demo || true
                    docker run -d --name docker-jenkins-demo -p 4000:4000 docker-jenkins-demo
>>>>>>> e34662a (Update Jenkinsfile)
                '''
            }
        }
    }
}
