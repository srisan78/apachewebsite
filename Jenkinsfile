pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'sridhar76/apachewebsite:latest'
    }

    stages {
        stage('Clone Git repository') {
            steps {
                git branch: 'main', url: 'https://github.com/srisan78/apachewebsite.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    credentialsId: 'ansible-ssh',
                    installation:
