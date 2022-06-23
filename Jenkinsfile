pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
                echo 'executing yarn...'
              nodejs('NodeJS-10-17') {
                   sh 'yarn install'
                }
            }
        }
        stage("build") {
            steps {
                echo 'executing gradle...'
              withGradle() {
                   sh './gradlew -v'
                }
            }
        }
    }
}
