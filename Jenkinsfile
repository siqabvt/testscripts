// Powered by Infostretch 

timestamps {

node ('master') { 

	stage ('02_Execute_WmTestSuite - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '85b39527-4e97-40ee-81cc-c7931285d8cf', url: 'https://github.com/siqabvt/testscripts']]]) 
	}
	stage ('02_Execute_WmTestSuite - Build') {
 			// Ant build step
 			if(isUnix()) {
 				sh "ant -buildfile \WmTestSuiteExecutor\run-composite-runner.xml -DwebMethods.integrationServer.ssl=false -DwebMethods.home=C:\\SoftwareAG -DwebMethods.test.setup.profile.mode=NONE -DwebMethods.integrationServer.name=dcssuv01 -DwebMethods.test.setup.location=C:\\Demo\\SampleTestSuite -DwebMethods.test.setup.external.classpath.layout=resources/test/classes,resources/java/classes,resources/test/jars,resources/java/jars,resources/jars -DwebMethods.integrationServer.port=7777 -DwebMethods.test.scope.packages=UnitTests -DwebMethods.integrationServer.userid=Administrator -DwebMethods.test.profile.result.location=C\:/Demo/WmTestSuiteExecutor/test/reports/ -DwebMethods.integrationServer.password=manage composite-runner-all-tests " 
			} else { 
 				bat "ant -buildfile \WmTestSuiteExecutor\run-composite-runner.xml -DwebMethods.integrationServer.ssl=false -DwebMethods.home=C:\\SoftwareAG -DwebMethods.test.setup.profile.mode=NONE -DwebMethods.integrationServer.name=dcssuv01 -DwebMethods.test.setup.location=C:\\Demo\\SampleTestSuite -DwebMethods.test.setup.external.classpath.layout=resources/test/classes,resources/java/classes,resources/test/jars,resources/java/jars,resources/jars -DwebMethods.integrationServer.port=7777 -DwebMethods.test.scope.packages=UnitTests -DwebMethods.integrationServer.userid=Administrator -DwebMethods.test.profile.result.location=C\:/Demo/WmTestSuiteExecutor/test/reports/ -DwebMethods.integrationServer.password=manage composite-runner-all-tests " 
			} 
	}
}
}