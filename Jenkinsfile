pipeline{
  agent any
    tools{
      maven 'Maven'
    }
    stages{
      stage('checkout')
      {
        steps{
          git branch: 'master',url:'https://github.com/Sonupriyankaramesh/MavenAnsibleWebApp1.git'
        }
      }
      stage('Build'){
        steps{
            sh 'mvn clean package '
        }
      }
      stage('Deploy with Ansible') {
            steps {
                sh 'ansible-playbook -i ansible/hosts.ini ansible/playbook.yml'
            }
      }
  }
  }
