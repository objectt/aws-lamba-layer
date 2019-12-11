# Using lxml, scrapy package on AWS Lambda

```
sudo yum -y update
sudo yum -y upgrade

cd /opt
sudo wget https://www.python.org/ftp/python/3.8.0/Python-3.8.0.tgz
sudo tar xzf Python-3.8.0.tgz
cd Python-3.8.0
sudo ./configure --enable-optimizations
sudo make altinstall

sudo yum install -y gcc libxml2-devel libxslt-devel
pip3.8 install --user virtualenv

cd ~
mkdir lambda
virtualenv env
source env/bin/activate

pip install lxml
pip install scrapy

zip -r9 py38-lxml-scrapy.zip env/lib/python3.8/site-packages
```
