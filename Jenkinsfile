pipeline {
    agent any
    options {
		timeout(time: "${BUILD_TIMEOUT}", unit: 'MINUTES') 
	 	disableConcurrentBuilds() 
	}

	triggers {
			pollSCM 'H * * * *'
	}
	stages {

        stage(" get source ") {
            when {
                expression {
                    env.GIT_BRANCH == 'develop' || env.GIT_BRANCH == 'master'
                }
            }
            agent none

			steps {
				sh """
                   			 echo test
				"""
			}
		}

	}
}
