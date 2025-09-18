pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/master-ankitt/jenkins-ansible-docker-app-deployment.git'
            }
        }

        stage('Deploy via Ansible to Node') {
            steps {
                sh '''
                # optional: verify ansible version or connectivity
                ansible --version

                # run the playbook
                ansible-playbook -i inventory app-deployment.yml
                '''
            }
        }
    }
}
