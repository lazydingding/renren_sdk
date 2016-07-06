# renren Python3 SDK

This SDK is a stand-alone Python script which provides

* API calling wrapper

for http://www.renren.com (renren.com)

Developed and mantained by Luping Yu. Please feel free to report bugs and
your suggestions at [here](https://github.com/lazydingding/renren_sdk).

## Installation

You can install the SDK via pip.

```
pip install renrensdk
```

## Get Access Token

### Recommended Approach ###
Step 1- Register Application

Register your open platform Application: [Register Application](http://app.renren.com/developers/newapp).

Step 2- Get Access Token

Visit [Renren Dev Tools](http://dev.renren.com/tools) to obtain access token

### Standard Approach (OAuth2 authentication) ###

English version for OAuth2.0 [OAuth2.0](http://open.renren.com/wiki/English_version_for_OAuth2.0).


OAuth 2 is a protocol focuses on client developer simplicity while providing
specific authorization flows for web applications.

There are many social networks provides OAuth 2 authentication and APIs, and
snspy is a simple API wrapper for any social network such as Twitter, Facebook,
LinkedIn, Sina Weibo, etc.

snspy provides a unique API interface for developers and difference of each
social network APIs are handled by its `mixin`.

## Initialize API instance

After setting up your Access Token, you can create the API instance now:

```python
from renren import API

access_token = [token1, token2, ...]

api = API(access_token)
```

## How to call a particular API (API 2.0)

The APIs are listed at [Renren API2 Documentation]
(http://open.renren.com/wiki/API2).
You can call an API using the APIClient's.  Remove "/v2/" and replace "/" with ".".  For example,

```python
print (api.profile.get(userId="383202003"))
print (api.friend.list(userId='383202003', pageSize=10000))
```
