node {

stage('SCM'){
 git 'https://github.com/estherviaud/devops_exercice_jenkins/edit/master/Jenkinsfile'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.97:9000/"
    }
}
