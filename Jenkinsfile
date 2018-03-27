pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        parallel(
          "checkout": {
            build(job: 'bluejob1', propagate: true, quietPeriod: 1)
            
          },
          "step2": {
            sleep 10
            
          }
        )
      }
    }
    stage('step3') {
      steps {
        parallel(
          "step3": {
            echo 'to step 3'
            
          },
          "step 4": {
            echo 'step 4'
            
          }
        )
      }
    }
  }
  environment {
    dev = 'dev'
  }
}