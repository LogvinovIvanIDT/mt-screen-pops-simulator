# psp-screen-pops-simulator

<p>This project contains configuration of mountbank server which emulates work of 
psp-screen-pops servers</p>

## Mock API

### PUT /screenpop/v1/calldata/did/{did}/ani/{ani}

| Path Template   |      Response Body      |  Status Code | Description |
|-----------------|:-----------------------:|:-------------|------------:|
| /screenpop/v1/calldata/did/[100]\d+/ani/[100]\d+ |   | 200 |This request save HttpRequest body to local cache. The body will be accessible from GET request Comment: did and ani should be a numerical and start from 100|


### GET /screenpop/v1/calldata/did/{did}/ani/{ani}

| Path Template   |      Response Body      |  Status Code | Description |
|-----------------|:-----------------------:|:-------------|------------:|
| /screenpop/v1/calldata/did/[100]\d+/ani/[100]\d+ |   | 200 |This request return the data which were loaded by PUT request before. Comment: did and ani should be a numerical and start from 100|
| /screenpop/v1/calldata/did/[200]\d+/ani/[200]\d+ |   | 200 |This request return the data which were loaded by PUT request before. Comment: did and ani should be a numerical and start from 200|
| /screenpop/v1/calldata/did/[500]\d+/ani/[500]\d+ |   | 500 |This request return the Http Request status 500 (Internal Server Error). Comment: did and ani should be a numerical and start from 500|
| /screenpop/v1/calldata/did/[404]\d+/ani/[404]\d+ |   | 404 |This request return the Http Request status 404 (Not Found). Comment: did and ani should be a numerical and start from 404|


<p>
The server uses 8082 http Port.
</p>