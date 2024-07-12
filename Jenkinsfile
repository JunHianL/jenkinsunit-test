pipeline {
	agent {
		docker {
			image 'composer-latest'
		}
	}
	environment {
        	DOCKER_TLS_CERTDIR = ''
        	DOCKER_HOST = ''
        }
	stages {
		stage('Build') {
			steps {
				sh 'composer install'
			}
		}
		stage('Test') {
			steps {
                sh './vendor/bin/phpunit tests'
            }
		}
	}
}