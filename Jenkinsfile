pipeline {
    //declare tools here in agent any tools section
    agent any
    tools{
        jdk 'java21'
        maven 'maven3'
    }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'feature-1', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Build') {
            steps {
                sh "mvn clean package -DskipTests=true"
                //DskipTests=true =>skips the test cases
            }
        }
        //Deploying application to tomcat
       
    }
}
