# mDrive
Provides access to local files on the device. Allows the user to add, edit, and remove files from a sharing catalog. Provides access to a shared media catalog.

# API Definition:

visit: https://app.swaggerhub.com/apis/mimik/mDrive/1.3.5

# Prerequisite

---

- You must have edgeEngine running and associated
- You must have mimik-edge-cli tool [More info](https://www.npmjs.com/package/@mimik/mimik-edge-cli)
- Use cli tool to retrieve your EDGE_ACCESS_TOKEN. You will need it for deployment

# Deployment

---

1. Download the latest release here: [mDrive releases](https://github.com/edgeMicroservice/mDrive/releases)
2. Use mimik-edge-cli to deploy the microservice

```
mimik-edge-cli image deploy --image={YOUR_IMAGE_PATH} --token={EDGE_ACCESS_TOKEN}
```

3. Once microservice is successfully deployed you should get output that looks like this:

```
created:  1626459503
digest:   sha265:b3b7652b2aa448de17bddf79463405fedfb1f43b0a17caaf4e8bbf11458e6400
id:       79279c04-8945-4141-8b52-2cb92b78cf43-mdrive-v1
name:     mdrive-v1
repoTags:
  - mdrive-v1:latest
size:     97587
status:   successfully deployed
```

4. Navigate to where 'start-mDrive.json' is located and run command:

```
mimik-edge-cli container deploy --payload start-mDrive.json --token={EDGE_ACCESS_TOKEN}
```

5. After successful container initialization you will get output similar to below:

```
clientId: 79279c04-8945-4141-8b52-2cb92b78cf43
created:  1626460485411
env:
  AUTHORIZATION_KEY:                  1234
  MCM.BASE_API_PATH:                  /79279c04-8945-4141-8b52-2cb92b78cf43/mdrive-v1/v1
  MCM.DB_ENCRYPTION_SUPPORT:          false
  MCM.LINKLOCAL_REPLAY_NONCE_SUPPORT: false
  MCM.WEBSOCKET_SUPPORT:              false
id:       79279c04-8945-4141-8b52-2cb92b78cf43-mdrive-v1
image:    mdrive-v1
imageId:  79279c04-8945-4141-8b52-2cb92b78cf43-mdrive-v1
name:     mdrive-v1
state:    started
```

- For more information and explanation, you can visit our [mCM container management API references](https://developer.mimik.com/edgeengine-mcm-api/) and [general guide on packaging, deployment, and exporting microservice](https://developer.mimik.com/building-edge-microservices/).
