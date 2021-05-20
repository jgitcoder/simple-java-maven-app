pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      arg '-v /root/.m2:/root/.m2'
    }
  }
  stages{
    stage('build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
  }
}
