// node('HRMS&&QA') {
//     stage('git') {
//         git 'https://github.com/dummyrepos/game-of-life.git'
//     }
//     stage('build') {
//         sh 'mvn clean package'
//     }
//     stage('testresults'){
//         junit 'gameoflife-web/target/surefire-reports/*.xml'
//     }
//     stage('archiveartifacts') {
//         archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
//     }
// }

pipeline {
    agent any 
    tools{
        jdk 'JDK-11'
        maven 'MAVEN-3.9.9'
    }
    stages{
        stage('SCM') {
            steps {
                git url: 'https://github.com/PrachiVpatil96/game-of-life.git'
            }
        }
        stage('Version') {
            steps {
                sh 'mvn --version'
            }
        }

        stage('validate'){
            steps {
                sh 'mvn validate'
            }
        }

        }
    }
