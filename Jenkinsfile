pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Check out your Ansible playbook and role code from your Git repository.
              git branch: 'main', url: 'https://github.com/pankaj0129/mysql_repo.git'
            }
        }

        stage('Deploy Role') {
            steps {
                script {
                    // Execute your Ansible playbook to deploy the role.
                    sh 'ansible-playbook -i aws_ec2.yml sites.yml'
                }
            }
        }
    }
}
