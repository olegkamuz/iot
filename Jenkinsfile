pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system
                git 'https://github.com/olegkamuz/iot'
            }
        }

        stage('Build') {
            steps {
                // Build the Maven project
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests if needed
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                // Package the Spring Boot application
                sh 'mvn package'
            }
        }

//         stage('Deploy') {
//             steps {
//                 // Deploy the application (e.g., to a server or container)
//                 // This step depends on your deployment strategy
//             }
//         }
    }

//     post {
//         success {
//             // Do something if the pipeline succeeds
//         }
//         failure {
//             // Do something if the pipeline fails
//         }
//     }
}