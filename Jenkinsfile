pipeline{
	agent any 
	stages{
		stage('Deployer Jfrog'){
				environment {
					MAVEN_HOME = '/usr/share/maven'
				}
			steps{
				
				rtMavenDeployer (
					id: 'DEPLOYADOR',
					serverId: 'lab2jfrog',
					releaseRepo: 'Laboratorio2',
					snapshotRepo: 'Laboratorio2',
				)
				rtMavenRun (
					pom: 'pom.xml',
					goals: 'install',
					deployerId: 'DEPLOYADOR'
				)
			}
		}
        }
}
