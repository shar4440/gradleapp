pipeline{
  agent any

  tools {
    gradle 'Gradle'
    jdk 'JDK'
  }
  stages{
    stage('checkout'){
      steps{
        git branch: 'master', url: 'https://github.com/shar4440/gradleapp.git'
      }
    }

    stage('build'){
      steps{
        sh 'gradle build'
      }
    }

    stage('test'){
      steps{
        sh 'gradle test'
      }
    }

    stage('steps'){
      steps{
      sh 'gradle run' 
    }
  }
}

  post{
    success{
      echo 'success'
    }
    failure{
      echo 'failed'
    }
  }
}
