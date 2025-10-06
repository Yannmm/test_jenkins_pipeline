pipeline {
    agent { label 'flutter' }

    stages {
        stage('Check Emulator') {
            steps {
                sh '''
                adb devices -l
                adb connect host.docker.internal:5555 || true
                adb devices -l
                '''
            }
        }
        // stage('Setup') {
        //     steps {
        //         sh 'node -v'
        //         sh 'npm -v'
        //         sh 'adb devices -l'
        //     }
        // }

        // stage('Install Dependencies') {
        //     steps {
        //         sh 'npm install'
        //     }
        // }

        // stage('Run Tests') {
        //     steps {
        //         sh 'npm test' // or your flutter test command
        //     }
        // }
    }
}
