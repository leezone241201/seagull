pipeline {
    agent any  // 选择执行环境，'any' 表示可以在任何可用节点上执行

    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'master', description: 'Branch to build')
    }
  
    stages {
        stage('Checkout') {
            steps {
                // 检出代码
                git branch: "${params.BRANCH_NAME}", url: 'git@github.com:leezone241201/seagull.git'
            }
        }

        stage('Build') {
            steps {
               echo '测试成昆'
            }
        }
    }


    post {
        success {
            // 构建成功后的步骤
            echo 'Build was successful!'
        }

        failure {
            // 构建失败后的步骤
            echo 'Build failed!'
        }
    }
}
