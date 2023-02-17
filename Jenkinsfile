pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build job: 'pes2ug20cs5-1'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/pes2ug20cs5-1/main/hello_exec'
            }
        }
      stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post{
      failure{
          echo 'pipeline failed'
      }
    }
}
