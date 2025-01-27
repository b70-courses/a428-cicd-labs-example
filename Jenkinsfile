node {
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {
        stage('Build') {
            try {
                sh 'npm installwrong'
            } catch (exception) {
                echo 'Failed when installing packages (npm install)'
                throw exception
            }
        }
        stage('Test') {
            try {
                sh './jenkins/scripts/testwrong.sh'
            } catch (exception) {
                echo 'Failed when running test scripts (test.sh)'
                throw exception
            }
        }
    }
}
