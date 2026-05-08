pipeline {

    agent any

    stages {

        stage('Install Apache') {
            steps {
                sh '''
                sudo yum install httpd -y
                '''
            }
        }

        stage('Copy Index File') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/
                '''
            }
        }

        stage('Give Permission') {
            steps {
                sh '''
                sudo chmod -R 777 /var/www/html/
                '''
            }
        }

        stage('Start Apache') {
            steps {
                sh '''
                sudo systemctl start httpd
                '''
            }
        }

    }
}
