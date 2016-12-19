//
// This Jenkinsfile is used for the "release" branches of a project (like master).
// We're not publishing artifacts and that's the only concern when using this for
// all branches.
//
properties([
  [$class: 'GitLabConnectionProperty', gitLabConnection: 'my-gitlab'],
  buildDiscarder(
    logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '15', daysToKeepStr: '', numToKeepStr: '')
  )
])

node() {
  checkout scm
  load "Jenkinsfile.common"
}
