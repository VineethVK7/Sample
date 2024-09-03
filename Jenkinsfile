pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/VineethVK7/Sample.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
                sh 'echo "Your HTML project doesn\'t require any build step!"'
            }
        }
        stage('Deploy') {
            steps {
                // Replace with the appropriate deployment command for your environment
                sh 'ibmcloud login --apikey 1Zfj6elYdOUO-fANDUvzlE6h0QTqjWVA3kpkIwYbnW7E'
                sh 'ibmcloud cos object-put --bucket vineeth190 --key index.html --file path/to/local/index.html'
            }
        }
    }
}
