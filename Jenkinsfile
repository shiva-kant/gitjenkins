pipeline {
    agent any

stages{
    stage('one'){
    steps{
        echo "Hello World"
    }
    }
    stage('parallel'){
    parallel{
        
        stage('two'){
            agent{
                label 'label1'
            }
            steps{
                echo "Hello @LABEL 1"
            }
        }
        stage('three'){
            agent{
                label 'label2'
            }
            steps{
                echo "Hello @label 2"
            }
        }
    }
    }
}

}
