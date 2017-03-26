# AWS Direct Upload Sample

Simple example demonstrating how to accomplish a direct upload to Amazon S3 in a Python Flask application.

Ideally the static assets are processed (minified / compressed) and served from a CDN instead of this app itself.

## Running the application

* Set environment variables for your AWS access key, secret, and bucket name
* Run:

    ```bash
    docker build -t aws-uploads-sample .
    docker run -d --name "uploader" -p 5000:5000 \
        -e "AWS_ACCESS_KEY_ID=${AWS_ACCESS_KEY_ID}" \
        -e "AWS_SECRET_ACCESS_KEY=${AWS_SECRET_ACCESS_KEY}" \
        -e "S3_BUCKET=${S3_BUCKET}" \
        aws-uploads-sample
    ```

* Visit [localhost:5000/upload](http://localhost:5000/upload) to try it out


## Source

This sample app is a direct copy of:

- [FlaskDirectUploader](https://github.com/flyingsparx/FlaskDirectUploader)
- [Direct to S3 File Uploads in Python](https://devcenter.heroku.com/articles/s3-upload-python)

## Licensing

The files in this repository are, unless stated otherwise, released under the Apache License. You are free to redistribute this code with or without modification. The full license text is available [here](http://www.apache.org/licenses/LICENSE-2.0).

