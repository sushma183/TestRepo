pipeline {
  agent any
  parameters {
    string(name:'A',defaultValue:'10',description:'First number')
    string(name:'B',defaultValue:'20',description:'Second number')
  }
  stages {
    stage('Test') {
      steps {
        echo 'Welcome to our first program'
      }
    }
    stage('Addition') {
      steps {
        sh '''
        a=1
        b=3
        echo 'Addition of $a and $b is $((a+b))'
        '''
      }
    }
    stage('Addition') {
      steps {
        sh '''
        python3 add.py
        '''
      }
    }
   stage('Parameterized addition') {
     steps {
       script {
         def sum = params.A.toInteger()+params.B.toInteger()
         echo 'Addition of $A and $B is $(sum)'
       }
     }
   }
  }
}

  
