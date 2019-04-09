---
UID: NS:http._HTTP_CONNECTION_LIMIT_INFO
title: HTTP_CONNECTION_LIMIT_INFO (http.h)
author: windows-sdk-content
description: Used to set or query the limit on the maximum number of outstanding connections for a URL Group.
old-location: http\http_connection_limit_info.htm
tech.root: http
ms.assetid: 6d2c1eeb-d248-4ca5-80b3-5c9f69ce8b9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PHTTP_CONNECTION_LIMIT_INFO, *PHTTP_CONNECTION_LIMIT_INFO structure [HTTP], HTTP_CONNECTION_LIMIT_INFO, HTTP_CONNECTION_LIMIT_INFO structure [HTTP], http.http_connection_limit_info, http/*PHTTP_CONNECTION_LIMIT_INFO, http/HTTP_CONNECTION_LIMIT_INFO"
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_CONNECTION_LIMIT_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_CONNECTION_LIMIT_INFO, *PHTTP_CONNECTION_LIMIT_INFO
req.redist: 
---

# HTTP_CONNECTION_LIMIT_INFO structure


## -description


The <b>HTTP_CONNECTION_LIMIT_INFO</b> structure is used to set or query  the limit on the  maximum number of outstanding connections for a URL Group.

 This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServerConnectionsProperty</a> on a URL Group.


## -struct-fields




### -field Flags

The <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.


### -field MaxConnections

The number of connections allowed. Setting this value to HTTP_LIMIT_INFINITE allows an unlimited number of connections.


## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

