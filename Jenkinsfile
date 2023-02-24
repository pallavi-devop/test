pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/pallavi/Documents/GRRAS/apache-maven-3.8.7/bin/mvn install'
	                 }}
		post {
		
			success{
				mail bcc: 'pallaviseo06@gmail.com', body: 'hi im from jenkins file', cc: 'pallaviseo06@gmail.com', from: '', replyTo: '', subject: 'project alert', to: 'pallaviseo06@gmail.com'
				}
		stage('Deployment'){
		    steps {
			
			sh 'cp target/project4.war /home/pallavi/Documents/GRRAS/apache-tomcat-9.0.71/webapps'
	}
}}}
