node {
     stage ('Checkout') {
    checkout scm
  }
  /*  stage('init') {
         Test Terraform 
           
            sh "terraform init -backend=true -input=false"
    } */
    stage('plan') {
            sh "terraform plan -out=tfplan -input=false"
    }  
    stage ('Terraform Apply') {
            sh 'terraform apply tfplan'
  }
}
