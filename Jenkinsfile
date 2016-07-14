#!groovy
stage 'setJAVA_HOME'
node {

     env.JAVA_HOME = "C:\\Program Files\\Java\\jdk1.8.0_91"

     echo env.JAVA_HOME
}
stage 'CLONE CASCADING'
node{
    git 'https://github.com/akankshaguha/CascadingProjectJenkins.git'
}
stage 'CLEAN PROJECT'
node{
     bat 'gradle clean'
}
stage 'BUILD PROJECT'
node{
     bat 'gradle build'
}
stage 'TEST'
node{
     bat 'gradle test'
}
stage 'RUN CUSTOM TASK'
node{
     bat 'gradle sayHello'
}