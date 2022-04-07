pipeline{
    agent any
    environment {
        // root = "go"
        branch = "main"
        scmUrl = "https://github.com/hariadiaf/sample-go-jenkins.git"
    }
    stages {
        stage("Git Clone") {
            steps {
                git branch: "${branch}", url: "${scmUrl}"
            }
        }
        
        stage("Go Dockerize") {
            steps {
                sh "docker build -t go-sample-jenkins ."
            }
        }
        
        stage("Deploy") {
            steps {
                echo "DEPLOY SUCCESS"
            }
        }        
    }
}