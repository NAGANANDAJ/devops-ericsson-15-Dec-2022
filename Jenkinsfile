pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    
    
    
        stage('Git CheckOut') {
            steps {
                git branch: 'main', url: 'https://github.com/amitvashisttech/devops-ericsson-15-Dec-2022.git'
            }
        }
    
    
  
        stage('Maven Clean') {
            steps {
                sh 'mvn clean -f 03-App-Code/my-app/pom.xml '
            }
        }
    
    
    
        stage('Maven Compile') {
            steps {
                sh 'mvn compile -f 03-App-Code/my-app/pom.xml '
            }
        }
    
    
    
        stage('Maven Test') {
            steps {
                sh 'mvn test -f 03-App-Code/my-app/pom.xml '
            }
        }
    
    
    
        stage('Maven Package') {
            steps {
                sh 'mvn package -f 03-App-Code/my-app/pom.xml '
            }
        }
    }
    
    
    
}
