pipeline {
    agent any

    // Check GitHub every minute for new commits.
    triggers {
        pollSCM('H/1 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application source code.'
                echo 'Tool: Apache Maven build automation tool.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests to verify individual functions and interactions between components.'
                echo 'Tools: JUnit for unit testing and Testcontainers for integration testing.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse the source code for code quality, reliability, maintainability and compliance with industry standards.'
                echo 'Tool: SonarQube static code analysis.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan the application and its dependencies to identify known security vulnerabilities.'
                echo 'Tool: Snyk vulnerability scanner.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a production-like staging server for validation.'
                echo 'Tools: AWS EC2 staging instance and Ansible deployment automation.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Execute integration and API tests against the application deployed in the staging environment.'
                echo 'Tool: Postman with the Newman command-line test runner.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the validated application to the production server.'
                echo 'Tools: AWS EC2 production instance and Jenkins deployment automation.'
            }
        }
    }
}
