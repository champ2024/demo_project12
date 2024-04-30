pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/champ2024/demo_project12.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook(
                    credentialsId: 'de360448-8a79-45f0-8681-35ce1faed6ee',
                    disableHostKeyChecking: true,
                    installation: 'ansible',
                    inventory: 'dev.inv',
                    playbook: 'copy.yml'
                )
            }
        }
    }
}
