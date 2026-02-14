pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo '📥 Checking out code...'
                // Code is automatically checked out
            }
        }
        
        stage('Environment Info') {
            steps {
                echo '🔍 Checking environment...'
                sh 'python3 --version'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        
        stage('Run Application') {
            steps {
                echo '🚀 Running application...'
                sh 'python3 hello.py'
            }
        }
        
        stage('Run Tests') {
            steps {
                echo '🧪 Running tests...'
                sh 'python3 test_hello.py -v'
            }
        }
    }
    
    post {
        success {
            echo '✅ Pipeline succeeded! Great job!'
        }
        failure {
            echo '❌ Pipeline failed! Check the logs.'
        }
        always {
            echo '🏁 Pipeline completed.'
        }
    }
}:wq

