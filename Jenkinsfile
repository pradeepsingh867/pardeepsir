pipeline{
agent{agent mynode} 
stages{
stage(checkout){
steps{
checkout
      }
       }
stage(build){
steps{
sh 'mvn package'
      }
              }
stage(sonar){
steps{
sonarqube.env(sonar){
sh 'mvn sonar:sonar'
}
      }
             }
stage(test){
steps{
sh ' junit .xml'
     }
           }
stage(nexus){
steps{
sh 'mvn deploy'
     }
            }
stage(deploy){
steps{
scp target/sample.war tomcat:webapps/
}
             }
post{
mail}
        }
stage9('build image')
{
dir (buildfolder)
 { 
sh 'docker build -t tomcat:$BUILD_NUMBER -F BUILDFOLDER'
SH 'docker push tomcat:$BUILD_NUMBER'
}
yum install ansible
root
scp source app@ip:dest
- hosts: hostgroupname
  tasks
  - name: copy a file
    copy: src=filename dest:foldername

