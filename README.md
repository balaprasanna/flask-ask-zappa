#### STEPS

1. Create aws credentials and store it under ~/.aws/credentials
```
[default]
aws_access_key_id={YOUR_ACCESS_KEY_ID}
aws_secret_access_key={YOUR_SECRET_ACCESS_KEY}
```

2. cd into project directory. Create a virtualenv inside the project directory.
```
virtualenv env
source env/bin/activate
```
FYI - To de-activate, type **deactivate**, to deactivate virtual env.

3. Install dependencies for the project, from requirments file
```
pip install -r requirements.txt
```

4. Prepare zappa. Lets init zappa.
```
zappa init
```
Follow the instuctions, you can leave it as defaults.

5. Deploy flask-ask using zappa.
```
zappa deploy dev
```
dev is the workspace, here.
It will take a minute to create a cloud formation template , and deploy the flask app as lamda function.

I love zappa. Its really awesome..
