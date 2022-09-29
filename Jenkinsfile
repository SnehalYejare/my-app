pipeline {
agent {
label {
label 'built-in'
customWorkspace '/data/pipeline'

}
}

stages {
//stage ('install-Apache-httpd')
//{
//steps {
//sh "yum install httpd -y"

//}

//}

stage ('deploy-index')

{
steps {
sh "cp -r index.html /var/www/html"
sh "chmod -R 777 /var/www/html/index.html"

}

}

stage ('Restart-Apache-httpd')
{
steps {
sh "systemctl restart httpd"


}

}

}
}
