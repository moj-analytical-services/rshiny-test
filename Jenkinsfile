#!groovy

pipeline {

  parameters {
    choice(
      name: 'IP_RESTRICTIONS',
      description: 'Whether the user needs to access the app from specific IPs',
      choices: 'DOM1\nDOM1 and QUANTUM\nDOM1, QUANTUM and 102 PF Wi-Fi\nDOM1, QUANTUM, 102 PF Wi-Fi and Clive House Wi-Fi\nAny location'
    )

    booleanParam(
      name: 'AUTHENTICATION_REQUIRED',
      description: 'Determine if the app requires authentication.',
      defaultValue: true
    )
  }

  agent any

  stages {

    stage('Deploy application') {
      steps {
        deploy()
      }
    }

  }
}
