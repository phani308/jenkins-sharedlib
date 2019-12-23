
stage('Prep') {
    script {
        // Create the release ID for this build
        def version = readFile('VERSION').trim()
        def buildID = env.BUILD_ID
        def shortSha = env.GIT_COMMIT.take(7)
        def prMetadata = ''

        if (env.CHANGE_ID) {
            prMetadata = "pr${env.CHANGE_ID}."
        }

        env.releaseID = "${version}+${prMetadata}.b${buildID}.${shortSha}"
      println "env.releaseID"
    }
}
