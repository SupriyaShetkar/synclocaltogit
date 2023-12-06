pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                // Compile the Java code
                sh 'javac HelloWorld.java'
            }
        }
       
        stage('Run') {
            steps {
                echo 'Running...'

                // Execute the Java program
                sh 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'All stages completed successfully!'
            // Additional actions upon successful build
        }
        failure {
            echo 'Pipeline failed :('
            // Additional actions upon failed build
        }
    }
}
