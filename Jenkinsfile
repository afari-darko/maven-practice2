node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=afari-darko_maven-webapp_cf35bea4-ea60-4a94-8a0b-9b45c2c4a0f3 -Dsonar.projectName='maven-webapp'"
    }
  }
}
