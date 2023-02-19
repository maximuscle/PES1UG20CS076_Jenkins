pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS066_test PES1UG20CS076_test.cpp'
        build job: 'PES1UG20CS076-1'
        echo 'Build stage done'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS076_test'
        echo 'Test stage done'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed successfully!!'
      }
    }
  }
  
  post{
    failure{
        echo "Pipeline failed!!"
    }
  }
}
