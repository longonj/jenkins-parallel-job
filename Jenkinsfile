pipeline{
	agent any 
	stages{
		stage('version-control'){
			steps{
				git checkout
			}
		}
		stage('parallel job'){
			parallel{
				stage('sub-job1'){
					steps{
						echo 'action1'
					}
				}
				stage('sub-job2'){
					step{
						echo 'action'
					}
				}
			}
		}
		stage('codebuild'){
			steps{
				sh 'cat/ets/passwd'
			}
		}
	}
}