pipeline {

agent any

stages {

stage('Clone Code') {
steps {
git 'https://github.com/username/netflix-devops-project'
}
}

stage('Build Docker Image') {
steps {
sh 'docker build -t username/netflix-app .'
}
}

stage('Push Image') {
steps {
sh 'docker push username/netflix-app'
}
}

stage('Deploy to Kubernetes') {
steps {
sh 'kubectl apply -f k8s/'
}
}

}

}
