pipeline{
    agent any
    tools{
        maven 'local_maven'
    }
    stages{
        stage ("Build"){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo "Archiving the Artifacts"
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }

    }
}