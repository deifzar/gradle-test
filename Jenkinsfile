@Library('devops-pipeline-libraries') _

gradleAndroidPipeline {
  environment             = 'dev'
  repoName                = 'gradle-test'
  scmProvider             = 'gitlab' // 'github' or 'gitlab'

  runTest                 = true
  runSAST                 = true // Sonarqube SAST
  runSCA                  = true
  runSBOM                 = true
  runDeployment           = true
  
  buildingImage           = 'cimg/android:2024.01'

  scaSeverity             = 'CRITICAL,HIGH'
  trivySkipDirs           = []
  trivySkipFiles          = []
  snykSkipDirs            = []
  snykSkipFiles           = []
  createPullOrMergeRequest = true

  gitCredentialsId        = 'gitlab-pat-jenkins' // gitlab-pat-jenkins || github-app-jenkins
  snykCredentialsId       = 'snyk-pat-jenkins'
  
  sonarqubeCredentialsId  = 'sonarqube-token'  // Jenkins credentials ID for SonarQube token 
  sonarqubeUrl            = 'https://sonarqube-cptm8net.spaincentral.cloudapp.azure.com'
  sonarqubeProjectKey     = 'Gradle-test' 
}
