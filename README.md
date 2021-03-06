# Rest-Api-Sample with Flask

## Starting

```
$ npm install -g serverless
$ serverless install --url https://github.com/Meenan21/Sampleapp-Python --name my-flask-app
$ cd my-flask-app && npm run setup
$ serverless deploy
```

Once the deploy is complete, run `sls info` to get the endpoint:

```
$ sls info
Service Information
<snip>
endpoints:
  ANY - https://abc6defghi.execute-api.us-east-1.amazonaws.com/dev <-- Endpoint
  ANY - https://abc6defghi.execute-api.us-east-1.amazonaws.com/dev/{proxy+}
```

Copy paste into browser.

## Local development

To develop locally, create a virtual environment and install your dependencies:

```
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```

Then, run your app:

```
sls wsgi serve
 * Running on http://localhost:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!
```

Navigate to [localhost:5000](http://localhost:5000) to see app running locally.

