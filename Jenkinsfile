@Library('my_shared-libraries') _

pipeline {
    agent any
    
    tools {
        maven "Maven_3.9.11"
    }


    stages {
        stage('Clone') {
            steps {
                gitClone('https://github.com/Nehad02/maven_pro.git')
            }
        }
        stage('Build'){
            steps{
                mavenBuild()
            }
        }
        stage('Code Review'){
            steps{
                sonarQube()
            }
        }
    }
}
