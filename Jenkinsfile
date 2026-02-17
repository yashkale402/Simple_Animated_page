pipeline {
    agent any

    stages{
        stage("Remove old code"){
            echo "Removing old code..."
            sh 'rm -rf /var/www/html/*'
        }
        stage("Checkout code"){
            echo "Checking out code from repository..."
            git url: 'https://github.com/yashkale402/Simple_Animated_page.git', branch: 'master'

        stage("Copy code to nginx directory"){
            echo "Copying code to nginx directory..."
            sh 'cp -r /var/lib/jenkins/workspace/Simple_Animated_page/* /var/www/html/'
        }

        stage("Deploy"){
            echo "Deploying the application..."
        }
    }
}