pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('Deploy') {
            steps {
                timeout(time: 3, unit: 'MINUTES') {
                    retry(5) {
                        echo "trying to deploy"
                    }
                }
           }
       }
       stage('Test') {
            steps {
                sh 'echo "Fail!"; exit 1'
            }
      }
    }
}
