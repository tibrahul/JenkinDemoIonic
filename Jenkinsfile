pipeline {
    agent any
        environment {
            PATH='/usr/local/bin:/usr/bin:/bin'
        }
        stages {
            stage('NPM Setup') {
            steps {
                sh 'npm install'
            }
        }

        stage('IOS Build') {
            steps {
                sh '“ionic cordova build ios --prod --release'
            } 
        }

        stage('APK Sign') {
            steps {
                // sh 'npm run apiSign'
                echo "Android"
            }
        }

        stage('Stage Web Build') {
            steps {
                sh 'npm run build --prod'
            }
        }

        stage('Publish Firebase Web') {
            steps {
                // sh 'firebase deploy --token "Your Token Key"'
                echo "Firebase Deploy"
            }
        }

        stage('Publish iOS') {
            steps {
                echo "Publish iOS Action"
            }
        }

        stage('Publish Android') {
            steps {
                echo "Publish Android API Action"
            }
        }

    }
}

