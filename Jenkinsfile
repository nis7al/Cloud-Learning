// this is th jenkins file for my new pipeline demo 
// i am learning the jenkins by writing declarative pipeline instead of scripted pipeline

pipeline {
    agent any 
    environment {
        GIT_REPO = "https://github.com/nis7al/Python-code-Library.git"
        GIT_BRANCH = "main"
        PYTHON_VERSION = 'pyhton3'
    }

    stages {
        stage('checkout') {
            steps {
                echo "this is the python compiler file"
                input("do you want to continue:")
                git branch: 'main', url : 'https://github.com/nis7al/Python-code-Library.git'
            }
        }

        stage(" dependendies install") {
            steps {
                script{
                if (fileExists('requirements.txt')){
                    sh "${PYTHON_VERSION} - m pip install requirements.txt"   
                }
             }
            }
        }
        stage('running the file') {
            steps {
                echo " this is th step of running th file for compiling"
                sh "${PYTHON_VERSION} main.py"
        }
        }
        
            
    }
}
