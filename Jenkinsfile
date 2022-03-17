pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build complited'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test complited'
          }
        }

        stage('test 1') {
          steps {
            echo 'test1 running'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'are you sure to deploy', ok: 'yes i a sure')
        echo 'deploy complited'
      }
    }

    stage('notify for new build') {
      steps {
        echo 'nex build'
      }
    }

  }
}