pipeline {
  agent any
  stages {
    stage("Install Rust")
    {
      steps {
        sh """
           curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs > install.sh
           chmod +x install.sh
           ./install.sh -y
       """
      }
    }
    stage('Build') {
      steps {
        sh "cargo build"
      }
    }

  }
}
