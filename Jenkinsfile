pipeline {
    agent any
    stages {
        stage ('Build da imagem Docker'){
            steps{
                sh 'docker build -t devops/app .'
            }
        }
        stage ('Subir docker compose - redis e app'){
            steps{
                sh 'docker-compose up --build -d'
            }
        }
        stage ('Sleep para subida de containers'){
            steps{
                sh 'sleep 10'
            }
        }
        stage ('Teste da aplicação'){
            steps{
                sh 'teste-app.sh'
            }
        }
    }
}