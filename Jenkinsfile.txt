pipeline {
    agent any
    stages {
        stage('Get_Playbook') {
            steps {
                git 'https://github.com/vishnukiranreddy4/ansiblerepo.git'
            }
        }
        stage('Run_Playbook') {
            steps {
                sh 'ansible-playbook playbook.yml'
            }
        }
    }
}
