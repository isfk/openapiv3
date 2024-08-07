# openapiv3

- `https://github.com/google/gnostic/tree/main/openapiv3`
- `https://github.com/google/gnostic/tree/main/cmd/protoc-gen-openapi`


```yaml
deps:
  - buf.build/isfk/openapiv3
```

## Usage

```proto
syntax = "proto3";

package api.v1;

import "openapiv3/annotations.proto";

option (openapi.v3.document) = {
  info: {
    title: "XXX API"
    version: "0.0.1-alpha"
    description: "XXX API Documentation"
    contact: {
      name: "xxx"
      url: "https://xxx.com"
      email: "xxx@live.cn"
    }
  }
  components: {
    security_schemes: {
      additional_properties: [
        {
          name: "BearerAuth"
          value: {
            security_scheme: {
              type: "http"
              scheme: "bearer"
            }
          }
        }
      ]
    }
  }
  security: [
    {
      additional_properties: [
        {
          name: "BearerAuth"
          value: {
            value: []
          }
        }
      ]
    }
  ]
};
```