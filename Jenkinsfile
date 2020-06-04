pipeline {

  agent { }
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/xiongye77/playjenkins.git', branch:'test-deploy-stage'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
