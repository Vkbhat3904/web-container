pipeline{
  agent any
  stages{
    stage("Clone"){
      steps{
        git "https://github.com/Vkbhat3904/web-container.git"
      }
    }
    stage("Build"){
      steps{
        bat "docker build -t cicd-static-app ."
      }
    }
    stage("Run Docker Container"){
      steps{
        bat "docker run -d -p 8082:80 --name web-container1 cicd-static-app"
      }
    }
  }
}