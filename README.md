# hexo-deployer-aliyun

Aliyun deployer plugin for [Hexo](http://hexo.io/).

## Installation

``` bash
$ npm install hexo-deployer-aliyun --save
```

## Options

You can configure this plugin in `_config.yml`.

``` yaml
# You can use this:
deploy:
  type: aliyun
  bucket: <yourBucketName>
  region: <yourOSSregion>
  accessKeyId: <yourAccessKeyId>
  accessKeySecret: <yourAccessKeySecret>
```

## Known Issues

Aliyun only finds `index.html` in root. This is [detail](https://help.aliyun.com/document_detail/31872.html?spm=5176.doc32081.2.2.aqynPK)

So you must set full url in your hexo blog codes like `/archives/index.html` except the root path.

## Unit Test

- SET Aliyun OSS ENV (OSS_BUCKET ...) IN `.env` file  

```
OSS_BUCKET   -> REQUIRED
OSS_REGION   -> REQUIRED
OSS_ACCESSKEYID  -> REQUIRED
OSS_ACCESSKEYSECRET -> REQUIRED
OSS_TIMEOUT  -> OPTIONAL
```

 - mocha test

```
npm install
mocha
```