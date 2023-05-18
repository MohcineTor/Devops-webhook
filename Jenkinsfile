pipeline{
agent any

stages{
stage("Clone Code"){
steps{
git branch : 'main', url:'https://github.com/MohcineTor/Devops-webhook.git'
}
}
stage("Build Code"){
steps{
sh 'docker build . -t django-todo-app:latest'
}
}
stage("Testing Code"){
steps{
echo "here some testing the code"
}
}
stage("Deploy Code"){
steps{
sh 'docker run -d -p 8000:8000 django-todo-app:latest'
}
}
}
}