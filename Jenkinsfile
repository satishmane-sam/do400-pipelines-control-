node('nodejs') {
    stage('Checkout') {
        git branch: 'main',
            url: 'https://github.com/satishmane-sam/do400-pipelines-control-'
//    }
 //   stage('Backend Tests') {
   //     sh 'node ./backend/test.js'
    //}
    //stage('Frontend Tests') {
    //    sh 'node ./frontend/test.js'
    //}
    stage('Run Tests') {
        parallel {
            stage('Backend Tests') {
                steps {
                    sh 'node ./backend/test.js'
                }
            }
            stage('Frontend Tests') {
                steps {
                    sh 'node ./frontend/test.js'
                }
            }
        }
    }
}
