pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t rohitrakshita/abinay:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 rohitrakshita/abinay:bus'
            }
        }
    }
}
