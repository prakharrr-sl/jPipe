node {
 	

    try {
      	stage ('Deploy') {
      	    git url: "git@github.com:prakharrr/jenkinsPipe.git",
                credentialsId: 'jenkins_ssh_key',
                branch: master
            steps{
                sh 'git tag -a tagName -m "Pushing with Jenkins" '
                sh 'git commit -am "merging with jenkinssss"'
                sh 'git push origin master'
            }

      	}
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}


