---
UID: NS:webservices._WS_CUSTOM_HTTP_PROXY
title: WS_CUSTOM_HTTP_PROXY (webservices.h)
description: A structure that is used to specify the custom proxy for the channel, using the WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY.
helpviewer_keywords: ["WS_CUSTOM_HTTP_PROXY","WS_CUSTOM_HTTP_PROXY structure [Web Services for Windows]","webservices/WS_CUSTOM_HTTP_PROXY","wsw.ws_custom_http_proxy"]
old-location: wsw\ws_custom_http_proxy.htm
tech.root: wsw
ms.assetid: cb666185-6a33-4e4c-a0b2-290f2f0bce4b
ms.date: 12/05/2018
ms.keywords: WS_CUSTOM_HTTP_PROXY, WS_CUSTOM_HTTP_PROXY structure [Web Services for Windows], webservices/WS_CUSTOM_HTTP_PROXY, wsw.ws_custom_http_proxy
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_CUSTOM_HTTP_PROXY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CUSTOM_HTTP_PROXY
 - webservices/_WS_CUSTOM_HTTP_PROXY
 - WS_CUSTOM_HTTP_PROXY
 - webservices/WS_CUSTOM_HTTP_PROXY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CUSTOM_HTTP_PROXY
---

# WS_CUSTOM_HTTP_PROXY structure


## -description

A structure that is used to specify the custom proxy for the channel, using 
                the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY</a>.

## -struct-fields

### -field servers

A semicolon-separated list of the proxy servers to be used by the channel. Each 
                    entry must follow the following EBNF.

``` syntax
<server>[":"<port>]
```


<ul>
<li>server=Address of the server
                    </li>
<li>port=TCP port number 
                    </li>
</ul>

### -field bypass

A semicolon separated list of servers which must be bypassed by the proxy. 
                    The bypass list can contain the string &lt;local&gt; to indicate that 
                    all local machine servers are bypassed.
