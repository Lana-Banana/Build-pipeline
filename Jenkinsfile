pipeline {
  agent any
  stages {
    stage('Gradle Build') {
      steps {
        echo 'Execute build.gradle '
      }
    }

    stage('Code Inspection') {
      steps {
        echo 'Integration Remote SonaQube'
        echo 'Call API to SoanrQube'
        echo 'Get Inspection Result From SonarQube'
      }
    }

    stage('Test') {
      steps {
        echo 'Run Test automation Script'
        echo 'Get test result'
      }
    }

    stage('Security Check') {
      steps {
        echo 'Integration With Remote Fortify'
        echo 'Get check result from remote Fortify'
      }
    }

    stage('Packaging') {
      steps {
        echo 'Make Jar snapshot'
        echo 'Build Docker image'
        echo 'Packaging Helm Chart'
      }
    }

    stage('Push to Repository') {
      steps {
        echo 'Push docker image to ECR'
        echo 'push helm chart package to Chart Museum'
        echo 'Push artifact to S3'
      }
    }

    stage('Deploy Request') {
      steps {
        input(message: 'Do you wanna trigger Deploy pipeline?', id: '1', ok: 'Yes', submitter: 'r.baek', submitterParameter: 'No')
      }
    }

  }
}