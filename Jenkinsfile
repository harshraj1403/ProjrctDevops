pipeline {
    agent any
    tools {
        nodejs "node"
    }
    stages {
        stage('Install Dependencies') {
            steps {
                git branch: 'main', credentialsId: 'GithubId',url: 'https://github.com/harshraj1403/ProjrctDevops.git'
               // sh 'npm install'
            }
        }
        stage('Install Node.js Dependencies') {
            steps {
                // Install Node.js dependencies
                bat 'npm install'
            }
        }
        stage('Start Next.js App') {
            steps {
                bat 'npm run &'
            }
        }
    }
}