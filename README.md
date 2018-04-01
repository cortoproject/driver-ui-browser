# driver-ui-browser
Plugin for browsing, monitoring and editing the corto hierarchy.

The `driver/ui/browser` plugin allows you to navigate the objects in a corto application. The browser provides access to all objects in an application, including the ones that are mounted from other datasources. The UI additionally allows for changing object values, and deleting objects.

## Configure the browser
To use the browser, simply install the `driver/ui/browser` package to your device. Then, make sure that your application configures both the `corto/ui` service (for serving up static files) and the `corto/ws` service (for serving up updates over websockets). The following example configuration starts both the ui and websocket service on port `9090`:

```json
[
    {
        "id": "config/ui",
        "type": "corto/ui/service",
        "value": {
            "port": 9090
        }
    },
    {
        "id": "config/ws",
        "type": "corto/ws/service",
        "value": {
            "port": 9090
        }
    }
]
```
