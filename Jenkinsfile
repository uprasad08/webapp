pipline{
   
   agent{ label 'slavelinux' }
   
      tools{
         maven 'Maven'
         jdk 'JAVA'
           }
   
   stages {      
     stage('Get the code from git')
         {
        steps{
            git credentialsId: '1fe00a2c-e680-48d6-ba8c-6abb51a0a561', url: 'https://github.com/uprasad08/webapp.git'
             }
         }     
      stage('build the source code')
         {
       steps{
           sh 'mvn clean install'
            }
         }    
      
     stage('send email')
        {
      steps{
          emailext body: '', subject: '', to: 'uprasad08@gmail.com'
           }
        }
      
     }
}
