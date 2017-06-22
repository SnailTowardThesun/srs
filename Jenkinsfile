pipeline {
    agent any
    stages {
        stage('config') {
            steps {
                sh 'cd trunk && ./configure'
            }
        }
        stage('build') {
            steps {
                sh 'cd trunk && make'
            }
        }
        stage('test') {
            steps {
                sh 'cd trunk && ./objs/srs_utest'
            }
        }
        stage('packet') {
            steps {
                sh 'cd trunk && ./scripts/package.sh --x86-x64'
            }
        }
    }
}
