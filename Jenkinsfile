pipeline{
    agent any

    stage {
            stage ('Compile Stage'){

                step{    
                    withMaven(maven : 'maven_384'){
                        sh 'mvn clean compile'
                    }
                }
            }

            stage ('Testing Stage'){

                step{
                    withMaven(maven: 'maven_384'){
                        sh 'mvn test'
                    }
                }
            }
            
            stage ('Deployment Stage'){

                step{
                    withMaven(maven: 'maven_384'){
                        sh 'mvn deploy'
                    }
                }
            }

    }
}