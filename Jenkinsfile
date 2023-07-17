node('JDK'){
    stage('SourceCode'){
        //get the code from the git repo.
        git branch: 'sprint', url: 'https://github.com/Reddy999eee/game-of-life.git'
    }
    stage('Build the code'){
        // building packge with shell script.
        sh 'mvn clean package'
    }
    stage('Archiving and Test Result'){
        junit '**/surefire-reports/.*xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }
}

