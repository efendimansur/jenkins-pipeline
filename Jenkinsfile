pipeline {
	agent any
    environment {
        AUTHOR = "Mansur Efendi"
        EMAIL = "kheva@gmail.com"
    }

    parameters {
        string(name: "Name", defaultValue: "Guest", description: "What is your name?")
        text(name: "Description", defaultValue: "Guest", description: "Tell about you")
        booleanParam(name: "Deploy", defaultValue: false, description: "Need to deploy?")
        choice(name: "SOCIAL_MEDIA", choices: ['Instagram', 'Facebook', 'Twitter'], description: "Which social media?")
        password(name: "SECRET", defaultValue: "", description: "Encrpt key")
    }

    options {
        disableConcurrentBuilds()
        timeout(time:100, unit: 'SECONDS')
    }
	stages {
        stage ("Build") {
            steps {
                echo "Hello ${params.name}"
                echo("Start Job: : ${env.JOB_NAME}")
                echo("Start Build: : ${env.BUILD_NUMBER}")
                echo("Branch Name: : ${env.BRANCH_NAME}")
                echo ("Author : ${AUTHOR}")
                sleep(20)
            }
        }

        stage ("Deploy"){
            steps {
                echo ("Deploy")  
                sleep(20)            
            }
        }
	}

    post {
        always {
            echo "I will always say Hello again!"
        }

        success {
            echo "sukses"
        }

        failure {
            echo "gagal"
        }
    }
}
