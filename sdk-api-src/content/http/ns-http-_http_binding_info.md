---
UID: NS:http._HTTP_BINDING_INFO
title: "_HTTP_BINDING_INFO"
author: windows-sdk-content
description: Used to associate a URL Group with a request queue.
old-location: http\http_binding_info.htm
tech.root: http
ms.assetid: 551a928a-84c6-479b-a500-de69dc8857cd
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PHTTP_BINDING_INFO, *PHTTP_BINDING_INFO structure [HTTP], HTTP_BINDING_INFO, HTTP_BINDING_INFO structure [HTTP], _HTTP_BINDING_INFO, http.http_binding_info, http/*PHTTP_BINDING_INFO, http/HTTP_BINDING_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - HTTP_BINDING_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_BINDING_INFO, *PHTTP_BINDING_INFO
req.redist: 
---

# _HTTP_BINDING_INFO structure


## -description


The <b>HTTP_BINDING_INFO</b> structure is used to associate a URL Group with a request queue.

This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServerBindingProperty</a> on a URL Group.


## -struct-fields




### -field Flags

The <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.


### -field RequestQueueHandle

The request queue that is associated with the URL group. The structure can be used to remove an existing binding by setting this parameter to <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

