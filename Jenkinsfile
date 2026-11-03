pipeline {
agent any

stages {

stage('Build') {
steps {
sh 'mvn compile'
}
}

stage('Test') {
steps {
sh 'mvn test'
}
}

stage('Package') {
steps {
sh 'mvn package'
}
}

stage('Deploy') {
steps {
sh '''
mkdir -p deploy
cp target/MavenDemo-1.0-SNAPSHOT.jar deploy/
java -cp deploy/MavenDemo-1.0-SNAPSHOT.jar App
'''
}
}
}
}
