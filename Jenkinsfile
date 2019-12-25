pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'Apache Maven 3.2.5'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'Apache Maven 3.2.5'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'Apache Maven 3.2.5'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
