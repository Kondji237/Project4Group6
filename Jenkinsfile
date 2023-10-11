pipeline{
	agent any 
	stages{
		stage(clonecode){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team7-git-id', url: 'https://github.com/Kondji237/Project4Group6.git']])
				}
			}
			parallel{
				stage('Divine'){
					steps{
						sh 'uname -a'
						sh 'lscpu'
					}
				}
				stage('Ngantcha'){
					steps{
						sh 'df -h'
						sh 'free -m'
					}
				}
			}
	}
}