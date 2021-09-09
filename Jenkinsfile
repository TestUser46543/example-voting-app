pipeline{
    agent any
    stages{
        stage('Checkout SCM'){
            steps{
                git url: 'https://github.com/Akshat1902/example-voting-app.git'
            }
        }
        stage('Run Docker Compose'){
            steps{
                echo "Running Job: ${env.JOB_NAME}\n build: ${env.BUILD_ID}"
                sh 'sudo chmod 666 /var/run/docker.sock'
                sh 'docker-compose --version'
                sh 'docker-compose up -d'
                sh 'docker ps -a'
            }
        }
    }
}

