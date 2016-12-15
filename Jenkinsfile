/**
* Android Jenkinsfile
*/
node('android') {
    stage 'Checkout'
    checkout scm

    stage 'Build'
    sh "./gradlew clean assembleDebug"

    stage 'Archive'
    archive 'app/build/outputs/apk/*.apk', excludes: 'app/build/outputs/apk/*-unaligned.apk'
}

