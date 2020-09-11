pipeline {
    agent any
    stages{
        stage("Build") {
            steps {
                echo "Building project..."
                sh 'Build.sh'
            }
            post {
                success {
                    echo "========Build successfully========"
                }
                failure {
                    echo "========Build failed========"
                }
            }
        }
        stage("Test") {
            steps {
                echo "Testing project..."
                sh 'Test.sh'
            }
            post {
                success {
                    echo "========Test successfully========"
                }
                failure {
                    echo "========Test failed========"
                }
            }
        }
        stage("Run") {
            steps {
                echo "Running project..."
            }
            post {
                success {
                    echo "========Run successfully========"
                }
                failure {
                    echo "========Run failed========"
                }
            }
        }
    }
    post {
        always {
            echo "========always========"
        }
        success {
            echo "========pipeline executed successfully ========"
        }
        failure {
            echo "========pipeline execution failed========"
        }
    }
}
