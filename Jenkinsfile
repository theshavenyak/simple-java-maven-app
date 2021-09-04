pipeline {
    agent {
        docker {
            image 'maven:3.8.2-adoptopenjdk-11-jdk-openj9' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
