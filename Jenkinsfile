node('master') {
    stage("Fetch Source Code") {
        git 'https://github.com/bhafez/Beginning-Jenkins.git'
    }

    dir('Lesson5') {
        printMessage('Running Pipeline')

        stage("Testing") {
            sh 'python test_functions.py'
        }
        
    stage("Deployment") {
        if (env.BRANCH_NAME == 'master') {
            printMessage('Deploying the master branch')
        } else {
            printMessage('No deployment configured for this branch')
        }
    }

        printMessage('Pipeline Complete')
    }
}

def printMessage(message) {
    echo "${message}"
}
