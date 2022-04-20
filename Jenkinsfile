pipeline{
    agent any

    tools {
         maven 'MAVEN_HOME'
         jdk 'JAVA'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url:'https://github.com/devopspractiece/mavenpro.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
