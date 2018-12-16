node ('master') { 
    stage ('scm-chekout')
    {
    checkout([$class: 'GitSCM', 
	branches: [[name: '*/master']], 
	doGenerateSubmoduleConfigurations: false, 
	extensions: [], submoduleCfg: [], 
	userRemoteConfigs: [[url: 'https://github.com/Pnirkhee/Radical_Project.git']]])
    }
    stage ('build') 
    {
      sh 'mvn -f pom.xml clean package'  
    }
}