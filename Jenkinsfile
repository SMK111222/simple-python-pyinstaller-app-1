pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                docker {
                    // 使用 Python 3 的 Alpine 镜像，体积小且现代
                    image 'python:3-alpine' 
                }
            }
            steps {
                // 编译 Python 文件为字节码
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}