# EventRule-Lambda-

sudo apt install python3

sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1

sudo update-alternatives --config python3

sudo apt-get install python3-pip

mkdir -p build/python/lib/python3.8/site-packages

pip3 install paramiko -t build/python/lib/python3.8/site-packages/ --system

cd /build

# zip the files

zip -r packageParamiko.zip .


# Upload zip file into S3

aws s3 cp packageParamiko.zip s3://<bucket-name>

Create Layer from the Zip file

Create a lambda function and upload the code and add necessary permissions for Lambda functions. Also increase the timeout of Lambda function.
