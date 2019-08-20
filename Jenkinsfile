node('Maven-Slave') {
    stage('FetchingSourceCode') {
        git credentialsId: '75547370-34be-4bd2-aaa4-78428286f93a', url: 'https://github.com/pavanpotluris/ycard.git'
    }
    stage('Test') {
        sh label: '', script: 'mvn clean deploy'
    }
    stage('Deploy') {
        build job: 'TestBuild1', quietPeriod: 5
    }
}
