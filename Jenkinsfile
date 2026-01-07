pipeline {
    agent any

    parameters {
        choice(
        
            name: 'ENV' , choices: ['QA', 'PROD' , 'DEV'] , description: 'Select Environment'
        )
    }

    stages {
        stage ('Chekout') {
            steps {
                checkout scm
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}