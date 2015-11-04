#Amazon EB deployment for Wercker.com

[![wercker status](https://app.wercker.com/status/a38256715b642c6833bbfff53e398272/m "wercker status")](https://app.wercker.com/project/bykey/a38256715b642c6833bbfff53e398272)

> Please note: This requires you to have an already existing Elastic Beanstalk application and environment in place, it will not run a startup procedure.

* `key` (required) Credentials key provided by amazon.
* `secret` (required) Credentials key secret provided by amazon
* `app_name` (required) Name of the application.
* `env_name` (required) Name of the application environment you wish to deploy to.
* `region` (optional) Region that your elastic beanstalk instance lives in, defaults to us-west-2.


```yml
deploy:
    steps:
        - hotakasaito/elastic-beanstalk-go-deploy:
            key: $AMAZON_KEY
            secret: $AMAZON_SECRET_KEY
            app_name: My Application
            env_name: production
            region: us-west-2
```
