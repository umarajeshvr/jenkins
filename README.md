
 stage('Checkoutbuild') {
        steps {
            sh 'mkdir -p build'
            dir("build")
            {
                git branch: "develop",
                credentialsId: 'uma',
                url: 'git@a.com:b/build.git'
            }
        }
    }

  stage('Checkoutpackage') {
        steps {
            sh 'mkdir -p package'
            dir("package")
            {
                git branch: "develop",
                credentialsId: 'uma',
                url: 'git@a.com:b/package.git'
            }
        }
    }
  stage('Checkoudeploy') {
        steps {
            sh 'mkdir -p deploy'
            dir("deploy")
            {
                git branch: "develop",
                credentialsId: 'uma',
                url: 'git@a.com:b/deploy
.git'
            }
        }
    }
