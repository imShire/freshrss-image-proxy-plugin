# freshrss-image-proxy-plugin
Based on the 2nd development of https://github.com/FreshRSS/Extensions/tree/master/xExtension-ImageProxy.

# Image Proxy extension

This FreshRSS extension allows you to get rid of insecure content warnings or disappearing images when you use an encrypted connection to FreshRSS. An encrypted connection can be [very easily enabled](http://fransdejonge.com/2016/05/lets-encrypt-on-debianjessie/) thanks to the [Let's Encrypt](https://letsencrypt.org/) initiative.

To use it, upload this entire directory to the FreshRSS `./extensions` directory on your server and enable it on the extension panel in FreshRSS.

## Configuration settings

* `proxy_url` (default: `https://images.example.com/?url=`): the URL that is prependended to the original image URL

* `proxy_white_list` (default: ``): whitelist, don't go proxy url

* `scheme_http` (default: `1`): whether to proxy HTTP resources

* `scheme_https` (default: `0`): whether to proxy HTTPS resources

* `scheme_default` (default: `auto`): which scheme to use for resources that do not include one; if set to `-`, those will not be proxied;
  if set along `scheme_include`, the scheme included in the URL will either be `auto`-matically derived from your current connection or the one explicitly specified

* `scheme_include` (default: `0`): whether to include the scheme - `http*://` - in the proxied URL

* `url_encode` (default: `1`): whether to URL-encode (RFC 3986) the proxied URL


## See Also

[ImageProxy](https://github.com/FreshRSS/Extensions/tree/master/xExtension-ImageProxy) plugin: Don’t need whiteList, proxy all url? Use ImageProxy plugin instead.

This extension is based on ImageProxy plugin, and is licensed under GPLv3.
