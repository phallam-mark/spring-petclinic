pipeline {
  agent { docker 'maven:3.5-alpine' }
    stages {
      stage('Checkout') {
        steps {
          git 'https://github.com/phallam-mark/spring-petclinic.git'
        }
      }
      stage('Build') {
        steps {
          sh 'mvn clean package'
          junit '**/terget/surefire-reports/TEST-*.xml'
        }
      }
    }
}
				 
