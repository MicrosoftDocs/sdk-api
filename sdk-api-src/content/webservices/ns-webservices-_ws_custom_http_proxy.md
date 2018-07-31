---
UID: NS:webservices._WS_CUSTOM_HTTP_PROXY
title: "_WS_CUSTOM_HTTP_PROXY"
author: windows-sdk-content
description: A structure that is used to specify the custom proxy for the channel, using the WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY.
old-location: wsw\ws_custom_http_proxy.htm
old-project: wsw
ms.assetid: cb666185-6a33-4e4c-a0b2-290f2f0bce4b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_CUSTOM_HTTP_PROXY, WS_CUSTOM_HTTP_PROXY structure [Web Services for Windows], _WS_CUSTOM_HTTP_PROXY, webservices/WS_CUSTOM_HTTP_PROXY, wsw.ws_custom_http_proxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_CUSTOM_HTTP_PROXY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CUSTOM_HTTP_PROXY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_CUSTOM_HTTP_PROXY structure


## -description


A structure that is used to specify the custom proxy for the channel, using 
                the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY</a>.
            


## -struct-fields




### -field servers

A semicolon-separated list of the proxy servers to be used by the channel. Each 
                    entry must follow the following EBNF.
                

<pre class="syntax" xml:space="preserve"><code>
&lt;server&gt;[":"&lt;port&gt;]</code></pre>

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


