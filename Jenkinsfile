pipeline {
    stages {
        stage ('Checkout') {
          steps {
            git 'https://github.com/docker-training/webapp.git'
          }
        }
        stage('Build') {
            steps {
                sh docker build -t devopsapr2021/myapp:${BUILD_NUMBER} .
            }
        }
        stage('publish') {
            steps {
                sh docker push devopsapr2021/myapp:${BUILD_NUMBER}
            }
        }
    }
}
