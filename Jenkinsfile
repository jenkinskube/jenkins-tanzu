pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/jenkinskube/jenkins-tanzu.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "sample-rails.yaml", kubeconfigId: "kubeconfig")
        }
      }
    }

  }

}
