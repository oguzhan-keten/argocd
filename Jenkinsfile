@Library('stagelibrary@master')_

pipeline {

    agent any

    options { 
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds() 
    }

    stages {
        stage("Build & Push") {
            steps {
              script {
                  stagelibrary.Build("argocd", "ArgoCd", BUILD_ID)
              }
          }
        }

       
    }
}