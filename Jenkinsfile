pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('create'){
steps{
git branch:'master',url:'https://github.com/PadmajaNaik14/MyMavenApp_test.git'
}
}
stage('build'){
steps{
sh 'mvn clean package'
}
}
stage('test'){
steps{
sh 'mvn test'
}
}
stage('run application'){
steps{
sh 'java -jar target/MyMavenApp_test-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'build success'
}
failure{
echo 'failed'
}
}
}
