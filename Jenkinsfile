pipeline{
agent any
// tools{
//     maven 'maven_3_5.2'
// }
stages{
    stage("Build"){
        steps{
            withDockerRegistry(
                [credentialsId:'dockertech',url:""]
                
            ){
                app = docker.build("neloeasybuggy")
        }
    }
            }
}
stage('Push'){
    steps{
        script{
            docker.withdockerregistry("https://457274511381.dkr.ecr.us-east-1.amazonaws.com", "ecr.us-east-1.amazonaws.com/neloeasybuggy")
        {
            app.push("latest")
        }


    }
}

}
