pipeline {
  agent any
  stages {
    stage('Docker Compose Up') {
      steps {
        sh 'docker-compose up -d'
      }
    }
    stage('Start files') {
      steps {
        sh 'curl http://localhost:9000/create_db.php'
        sh 'curl http://localhost:9000/create_table.php'
        sh 'curl http://localhost:9000/getting_data.php'
        sh 'curl http://localhost:9000/insert_data.php'
        sh 'curl http://localhost:9000/remove_data.php'
        sh 'curl http://localhost:9000/remove_db.php'
      }
    }
  }
}
