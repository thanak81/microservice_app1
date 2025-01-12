pipeline {
    agent any;
    stages {
        stage ("Check condition"){
            steps {
                script {
                    if(sh(script: "git diff --name-only HEAD~1 HEAD ./frontend", returnStdout: true).trim()){
                        echo "Change detected in frontend"
                    }
                     if(sh(script: "git diff --name-only HEAD~1 HEAD ./catalogue", returnStdout: true).trim()){
                        echo "Change detected in catalogue"
                    }
                       if(sh(script: "git diff --name-only HEAD~1 HEAD ./voting", returnStdout: true).trim()){
                        echo "Change detected in voting"
                    }
                }
            }
        }
    }
}