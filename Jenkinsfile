node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("xavki/nginx")
    }

    stage('Run image') {
        docker.image('xavki/nginx').withRun('-p 80:80') { c ->

        batch 'docker ps'

        batch 'curl localhost'

    }

    }
    
}
