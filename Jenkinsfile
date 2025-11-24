pipeline {
    agent any

    environment {
        K8S_NAMESPACE = "default"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Tests') {
            steps {
                sh 'echo "TODO: add tests"'
            }
        }

        stage('Deploy to k3s') {
            steps {
                sh '''
                echo "Deploy nach k3s..."
                kubectl apply -n $K8S_NAMESPACE -f k8s/
                kubectl get pods -n $K8S_NAMESPACE
                '''
            }
        }
    }
}
