pipeline {
    agent {
        docker {
            image 'quay.io/buildah/stable'
            args '--rm --name=buildahctr --net=host --security-opt label=disable --security-opt seccomp=unconfined --device /dev/fuse:rw -v /mnt/data/mycontainer:/var/lib/containers:Z'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'ls -l; buildah -v'
            }
        }
    }
}
