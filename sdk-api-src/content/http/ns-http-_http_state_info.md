---
UID: NS:http._HTTP_STATE_INFO
title: "_HTTP_STATE_INFO"
author: windows-sdk-content
description: Used to enable or disable a Server Session or URL Group.
old-location: http\http_state_info.htm
old-project: http
ms.assetid: 736ae89b-a4fb-4962-ae68-9aaccd869c88
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_STATE_INFO, *PHTTP_STATE_INFO structure [HTTP], HTTP_STATE_INFO, HTTP_STATE_INFO structure [HTTP], _HTTP_STATE_INFO, http.http_state_info, http/*PHTTP_STATE_INFO, http/HTTP_STATE_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HTTP_STATE_INFO, *PHTTP_STATE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_STATE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_STATE_INFO structure


## -description


The <b>HTTP_STATE_INFO</b> structure is used to enable or disable a Server Session or URL Group.

This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServerStateProperty</a> on a URL Group or Server Session.


## -struct-fields




### -field Flags

The <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.


### -field State

A member of the <a href="https://msdn.microsoft.com/15e27788-2d1a-4818-b31f-2faf649e15b2">HTTP_ENABLED_STATE</a> enumeration specifying the whether the configuration object is enabled or disabled.

This can be used to disable a URL Group or Server Session.


## -remarks



When the <b>HttpServerStateProperty</b> is set on a server session or a URL group, the <b>HTTP_STATE_INFO</b> structure must be used. Server Sessions, and URL Groups represent a configuration for a part of the namespace where inheritance is involved.  When traversing the namespace for a request, the HTTP Server API may encounter multiple applicable URL Groups. The property configuration structures must carry information identifying if it is present in a specific URL group.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

