pipeline {
	agent any
	environment{
		registry = boopathy102/emart
		registryCredential = 'dockerHub'
		dockerImage = ''
	}
	stages{
		stage("checkout"){
			steps{
				git branch:'main', url:'git@github.com:Boopathy02/emartapp.git'
			}
		}
		stage('docker image'){
			steps{
				script{
					dockerImage = docker.build registry + ":$BUILD_NUMBER"
				}
			}
		}
	}
}