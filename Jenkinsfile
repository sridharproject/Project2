pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git credentialsId: 'GITHUB_CRED', url: 'https://github.com/sridharproject/Project2.git', branch: 'main'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook tomcat-deploy.yml'
            }
        }
    }
}
