pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
	stage('Test') {
	    steps {
		sh 'echo "runing test"'
	    }
	    post {
	    	always {
		    echo 'This will always run'
	    	}
		success {
            	    echo 'This will run only if successful'
        	}
	    }
	}
    }
}

