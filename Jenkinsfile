pipeline {
    agent { label 'ads01' }
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/shankar1016/javaproj.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

        
    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
