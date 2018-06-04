---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


