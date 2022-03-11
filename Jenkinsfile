pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
            
                checkout([$class: 'GitSCM',
          branches: [[name: 'master']],
          extensions: [],
          userRemoteConfigs: [[url: 'https://github.com/krithiv2012/ansible_demo']]])
            dir('playbooks'){
                ansiblePlaybook(inventory: 'dev', playbook: 'test.yml')
                
            }
            }
        }
    }
}

