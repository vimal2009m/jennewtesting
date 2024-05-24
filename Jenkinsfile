pipeline {
    agent any
    stages {
        stage ('Git Clone') {
            steps {
                git(
                    url: "https://github.com/vimal2009m/jenrepo-2024ms.git",
                    branch: "main",
                    changelog: true,
                    poll: true
                )
        }    }
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
