pipeline
{
agent any
stages
{

stage('scm checkout')
{
    steps 
    { 
        git branch: 'main', url: 'https://github.com/diyakashyap/simple-java-maven-app.git' 
    }
}


stage('Build the code')
 {
    steps 
    { 
        withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_home', maven: 'Maven_home', mavenSettingsConfig: '', traceability: true) 
        {
            sh 'mvn package'
        } 
    }
}
}
}
