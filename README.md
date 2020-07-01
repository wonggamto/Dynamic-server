```
  var get_cookies = function(request) {
    var cookies = {};
    request.headers && request.headers.cookie.split(';').forEach(function(cookie) {
        var parts = cookie.match(/(.*?)=(.*)$/)
        cookies[parts[1].trim()] = (parts[2] || '').trim();
    });
    return cookies;
}
const myCookie = get_cookies(request)['logined']
```
### 通过网上找的答案解决了获取不了cookie的问题
### 获取cookie出现问题，会多出一个webstorm和一个pycharm的cookie
# static-server
改良版的server.js，做了一些调整，通过数据结构根据后缀自动匹配文件类型
