pipeline {
  agent any
  stages {
    stage('Build') { 
      steps {
         sh ./gradlew build --no-daemon
      }
    }
   }
  post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}
}
