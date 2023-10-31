pipeline {
 agent {
  label 'slave1'
}
stages {
  stage('git checkout') {
    steps {
     git 'https://github.com/Shivayogi-k/onlinebookstore.git'
    }
  }

  stage('build stage') {
    steps {
      sh 'mvn clean install'
    }
  }

  stage('deploy') {
    steps {
     sh 'sudo cp -r target/*.war /opt/tomcat/apache-tomcat-9.0.68/webapps'
    }
  }

}

    
}
