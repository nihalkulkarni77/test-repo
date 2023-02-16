pipeline{
	agent{
		label {
			label 'built-in'
		}
	}
	
	stages{
		stage ('clone-test-repo'){
			steps {
				dir ('/mnt/projects'){
					sh "sudo rm -rf test-repo"
					sh "sudo git clone https://github.com/nihalkulkarni77/test-repo.git"
				}
			}
		}
		
		stage ('copy-index-file'){
			steps {
				sh "rm -rf /var/www/html/index.html"
				sh "cp /mnt/projects/test-repo/index.html /var/www/html"
			}
		}
	}	
	
}
