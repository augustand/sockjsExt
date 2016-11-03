# sockjsExt
让sockjs或者websocket用的和socketIO一样爽


```
function test() {
    withSockJS("/echo", function (ws) {
        ws.on("open", function (msg) {
            ws.emit("name", "data");
        });

        ws.on("jjjj", function (msg) {
            ws.emit("name", "data", function (msg) {
            });
        });
    });

    var ws = new SockJSWrap("/echo");
    ws.on("jjjj", function (msg) {
        ws.emit("name", "data", function (msg) {
        });
    });
}
```