pipeline {
    agent any

     environment {
        NODEJS_VERSION = '18' // Update this to the latest LTS version of Node.js
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git   
                git 'https://github.com/beingviksa/react-city-tour.git'
            }
        }
        
        stage('Build') {
            steps {
                // Install Node.js and dependencies
                sh 'curl -sL https://deb.nodesource.com/setup_18.x | bash -'
                sh 'apt-get install -y nodejs'
                sh 'npm install'
                
                // Build the React app  
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests (you may need to modify this based on your testing framework)
                sh 'npm test'
            }
        }
        
        stage('Complete') {
            steps {
                sh 'Success'
            }
        }
    }
}
