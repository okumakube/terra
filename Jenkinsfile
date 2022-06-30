pipeline {
  agent any
  tools {
      terraform "Terraform1.0.0"
  }

  stages {
    stage('Git Checkout') {
      steps {
        git credentialsId: '16**-**-**-**-**cb', url: 'https://git-codecommit.us-west-2.amazonaws.com/v1/repos/TerraformJenkins'
      }
    }

    stage('Terraform Init') {
      steps {
        sh label: '', script: 'terraform init'
      }
    }
    
    stage('Terraform apply') {
      steps {
        sh label: '', script: 'terraform apply --auto-approve'
      }
    }
  }
}
