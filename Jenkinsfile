pipeline {
    agent {
        node {
            label 'Windows1' 
        }
           }

    stages {
        stage('Compile') {
            steps {
                echo 'compiling..'
                bat 'mvn compile'
            }
        }
        stage('codereveiw') {
            steps {
                echo 'reveiw..'
                bat 'mvn pmd:pmd'
            }
        }
        stage('test') {
            steps {
                echo 'Testing....'
                bat 'mvn test'
            }
        }
        stage('Metricheck') {
            steps {
                echo 'metricheck....'
                bat 'mvn cobertura:cobertura'
            }
        }
        stage('build') {
            steps {
                echo 'testing....'
                bat 'mvn package'
            }
        }
    }
}
