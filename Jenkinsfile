pipeline{
    agent {
        label 'slave1'
}
    tools {
         maven 'maven-tool'
}
  stages {
      stage('git checkout'){
          steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sadiq-inamdar/hello-world.git']]])
          }
      }
      stage('Build SourceCode'){
           steps{
               sh 'mvn clean package'
           }
       }
  }

}
