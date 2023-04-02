node {
    def app
    stage('Clone repository') {
        checkout scm
    }
    stage('Build image') {
       app = docker.build("jana-i/kiii-jenkins-new")
    }
   stage('Push image') {
        withDockerRegistry([ credentialsId: "docker-hub-credentials", url: "" ]) {
        bat "docker push devopsglobalmedia/teamcitydocker:build"
        }
}
