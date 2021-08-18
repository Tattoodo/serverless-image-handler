# SHELL := /bin/bash

build:
	./build-s3-dist.sh serverless-image-handler-imgix serverless-image-handler-imgix $(VERSION)

sync-assets-staging:
	aws s3 sync ./global-s3-assets/ s3://serverless-image-handler-imgix-eu-central-1/serverless-image-handler-imgix/$(VERSION) --acl bucket-owner-full-control;
	aws s3 sync ./regional-s3-assets/ s3://serverless-image-handler-imgix-eu-central-1/serverless-image-handler-imgix/$(VERSION) --acl bucket-owner-full-control

sync-assets-production:
	aws s3 sync ./global-s3-assets/ s3://serverless-image-handler-imgix-us-east-1/serverless-image-handler-imgix/$(VERSION) --acl bucket-owner-full-control;
	aws s3 sync ./regional-s3-assets/ s3://serverless-image-handler-imgix-us-east-1/serverless-image-handler-imgix/$(VERSION) --acl bucket-owner-full-control
