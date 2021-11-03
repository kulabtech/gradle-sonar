pipeline {
 agent any
 tools{
     gradle 'gradle'
      }
     stages{
         stage('CheckoutCode')
          {
            steps
             {
                git credentialsId: 'git_creds', url: 'https://github.com/kulabtech/gradle-sonar.git' , branch: 'main'
             }
          }
         stage ('Build') 
         {
            steps 
            {
                sh 'chmod +x gradlew'
                sh './gradlew clean build'
            }
        }
     }
}
