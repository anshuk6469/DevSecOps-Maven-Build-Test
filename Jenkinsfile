pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven_new"
    }

    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/anshuk6469/nodejs-app2.git'
                sh "mvn clean package -DskipTests=true"
            }
        }
           stage('Unit-Test') {
            steps {
                sh "ls ; mvn test"
            }
        }
    }   
}
}
