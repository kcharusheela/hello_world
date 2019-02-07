node {
   stage('Checkout Code') {
      git 'https://github.com/kcharusheela/hello_world.git'
   }
   stage('Unit Test') {
      // run the unit tests
      dir("hello_world") {
         sh "virtualenv .env"
         sh ". .env/bin/activate"
         sh "pip install -r /root/gitrepo/hello_world/ requirements.txt"
         sh "python -m pytest tests/test_app.py"
      }
   }
}
