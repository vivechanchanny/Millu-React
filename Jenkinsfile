pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo su"
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo su"
                sh "sudo rm -rf /usr/share/nginx/html/"
                sh "sudo su"
                sh "sudo cp -r ${WORKSPACE}/build /usr/share/nginx/html/"
            }
        }
    }
}
