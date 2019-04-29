# Basic usage of data APIs

```js
const { DataManagementClient, AuthenticationClient } = require('forge-nodejs-utils');
const data = new DataManagementClient(new AuthenticationClient());

const buckets = await data.listBuckets();
console.log('Buckets', buckets.map(bucket => bucket.bucketKey).join(','));

const objects = await data.listObjects('foo-bucket');
console.log('Objects', objects.map(object => object.objectId).join(','));
```