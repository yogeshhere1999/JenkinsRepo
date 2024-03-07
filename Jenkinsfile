pipeline {
    agent any
    
	 stages {
		        stage('Checkout') {
		            steps {
		                // Checkout code from the Git repository
				 git branch: 'master', url:'https://github.com/debdan0341/Jenkins.git'

		                echo 'checkout'
		              }
		           }
		        
		        stage('Build') {
		            steps {
		                // Build Selenium project using Maven
				    dir('.'){
				        echo 'build'
				        bat 'mvn clean'
				    }
		             }
		          }
        
		        
        
		     
        
          }
    
    post {
	        always {
			// Cleaning  up tmp
			
	            echo 'This is for post section'
	        }
        
	        success {
	            // Actions when pipeline succeeds
	            echo 'Pipeline is Successful!'
	        }
        
	        failure {
	            // Actions when pipeline fails
	            echo 'Pipeline is Failed!'
	        }
          }
	
}
