scrippies/aws-cheatsheet.md
===========================

# s3

## create bucket

```
$ aws s3 mb s3://this.is.my.bucket --region us-east-1
make_bucket: this.is.my.bucket
```

## block public access

```
$ aws s3api put-public-access-block \
>     --bucket this.is.my.bucket \
>     --public-access-block-configuration \
>     "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=true,RestrictPublicBuckets=true"
```
