
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting project code'
                checkout scm
            }
        }

        stage('Test') {
            steps {
                echo 'Running Python tests'
                 bat '"C:\\Users\\admin\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" --version'
                 bat '"C:\\Users\\admin\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m unittest discover -s . -p "test_*.py" -v'                
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline Successful!'
        }

        failure {
            echo 'CI Pipeline Failed!'
        }
    }
}