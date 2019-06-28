pipeline {
  agent any
  freeStyleJob('NexusArtifactUploaderJob') {
    steps {
      nexusArtifactUploader {
        nexusVersion('nexus2')
        protocol('http')
        nexusUrl('localhost:8081')
        groupId('sp.sd')
        version('3.16')
        repository('Test')
        credentialsId('nexus-credencial')
        artifact {
            artifactId('nexus-artifact-uploader')
            type('jar')
            classifier('debug')
            file('nexus-artifact-uploader.jar')
        }
      }
    }
}
}
