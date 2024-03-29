# eodhistoricaldata API

This project provides a set of functions to receive data from the
eodhistoricaldata website via their
[API](https://eodhistoricaldata.com/knowledgebase/). This project is licensed
under Apache 2.0 or MIT license (see files LICENSE-Apache2.0 and LICENSE-MIT).

# Usage
Please note that you need to have a registered account with eodhistoricaldata to
receive an individual API token. The most basic account is free but limited to
EOD Historical Data and LIVE/Realtime Data only and allows only 20 requests per day. 

Since version 0.3 and the upgrade to ```reqwest``` 0.10, all requests to the
yahoo API return futures, using ```async``` features. Therefore, the functions
need to be called from within another ```async``` function with ```.await``` or
via funtions like ```block_on```. The examples are based on the ```tokio```
runtime applying the ```tokio-test``` crate.
