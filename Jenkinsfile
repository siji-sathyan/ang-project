pipeline {
    agent {label 'agent' }
    
    tools {
    nodejs 'NodeJS'
    } 
    environment {
        CI = 'true'
    }

    stages {
        stage('checkout') {
            steps {
                
                git branch:'master', url:'https://github.com/sreejuss/Angular-Jenkins.git'
                
            }
        }
         stage('npm install') {
            steps {
                
               sh 'npm install'
                
            }
        }
         stage('build') {
            steps {
                
              sh 'npm run build'
              archiveArtifacts artifacts: '/dist/**/*.zip', followSymlinks: false
                
            }
        }
    }
}


