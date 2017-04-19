pipeline {
  agent {
    docker {
      image 'warchantua/iroha-dev'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh '''mkdir build
cd build
cmake ..
make -j2'''
      }
    }
    stage('Test') {
      steps {
        sh 'ctest'
      }
    }
  }
}