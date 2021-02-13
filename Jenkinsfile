pipeline {
    agent { dockerfile true }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'docker build -t juno0812/HelloWorld .'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'docker run -p 8081:8080 -d juno0812/HelloWorld'
                curl localhost:8081
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
