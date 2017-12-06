properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/Outsource-demo/Design.git'],
    pipelineTriggers([githubPush()])])
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
            }
        }
        stage ('Downstream-test'){
			steps {
     				build job: 'Outsource-demo/Development/master'
			}
		}
    }
}
