@Library('my-shared-library@main') _

pipeline {
  agent any
 
  tools {maven "MyMaven" 
         nodejs "nodejs"
        dockerTool "myDocker"}
  
  parameters {
        string(name: 'url', defaultValue: 'https://github.com/tapasmishraarc/SpringbootdemoPOC.git', description: 'My application url')
    }
  stages {
    stage('CI-Pipeline') {
      steps {
        script {
         // comment added new2
        //readProperties "${params.url}", this
       // echo "${env.APP_NAME}"
         build  "${params.url}", this
        }
        
      }
    }
  }
}

