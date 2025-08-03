pipeline {
  agent any
  stages {
    stage('Clone Git Repository') { 
       steps {
         git branch: 'main', url: 'https://github.com/Kunal-J2307/ansible-jenkins-demo'
       }
    }

    stage('Run Ansible Playbook') { 
       steps {
         ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory file.ini', playbook: 'playbook.yml', vaultTmpPath: ''
       }
    }
  }
}
