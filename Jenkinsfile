pipeline{
  agent any
  tools{
    maven'Maven'
  }
  stages{
    stage('CheckOutline'){
      steps{
        git branch:'main',url:'https://github.com/RISHI152-stack/devopstestmaven.git'
      }
    }
    stage('Build'){
      steps{
        sh'mvn-clean-package'
      }
    }
    stage('Test'){
      steps{
        sh'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        sh'java -jar target/SIMPLEMAVEN-1.0-SNAPSHOT.jar
'
      }
    }
  }

  post{
    success{
      echo'build and deployment success'
    }
    failure{
      echo'failed'
    }
  }
}
