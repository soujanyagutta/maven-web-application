node {
    def mavenHome=tool name:"maven3.6.2"
stage ( 'checkoutcode' ){
git branch: 'development', credentialsId: 'abced4b2-40e3-4849-90fa-6b09ebe6cc39', url: 'https://github.com/soujanyagutta/maven-web-application.git'
}
stage ( 'Build' ){
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage ( 'executeSonarQubeReport' ){
sh  "${mavenHome}/bin/mvn sonar:sonar"
}
stage ( 'uploadArtifactIntoRepo' ){
sh  "${mavenHome}/bin/mvn deploy"
}
stage ( 'deployApplicationIntoTomcat' ){
sshagent(['ad569ef3-1eca-4192-a161-4ce1320490e1']) {
    sh "scp  -o StrictHostKeyChecking=no  target/maven-web-application.war ec2-user@3.108.252.194:/opt/apache-tomcat-9.0.50/webapps/"
}
}
stage ( 'sendEmailNotification' ){
emailext body: '''Build Done
Regards
Soujanya Gutta''', subject: 'build over', to: 'soujanyagutta1993@gmail.com,sjes4444@gmail.com,sowjanyagutta94@gmail.com'
}
*/
}
