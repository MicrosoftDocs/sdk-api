---
UID: NS:http._HTTP_BANDWIDTH_LIMIT_INFO
title: "_HTTP_BANDWIDTH_LIMIT_INFO"
author: windows-sdk-content
description: The HTTP_BANDWIDTH_LIMIT_INFO structure is used to set or query the bandwidth throttling limit. This structure must be used when setting or querying the HttpServerBandwidthProperty on a URL Group or server session.
old-location: http\http_bandwidth_limit_info.htm
tech.root: Http
ms.assetid: 34c85ecf-1eb4-4f0d-a081-4b9feeb8dd15
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PHTTP_BANDWIDTH_LIMIT_INFO, *PHTTP_BANDWIDTH_LIMIT_INFO structure [HTTP], HTTP_BANDWIDTH_LIMIT_INFO, HTTP_BANDWIDTH_LIMIT_INFO structure [HTTP], _HTTP_BANDWIDTH_LIMIT_INFO, http.http_bandwidth_limit_info, http/*PHTTP_BANDWIDTH_LIMIT_INFO, http/HTTP_BANDWIDTH_LIMIT_INFO"
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
 - HTTP_BANDWIDTH_LIMIT_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_BANDWIDTH_LIMIT_INFO, *PHTTP_BANDWIDTH_LIMIT_INFO
req.redist: 
---

# _HTTP_BANDWIDTH_LIMIT_INFO structure


## -description


The <b>HTTP_BANDWIDTH_LIMIT_INFO</b> structure  is used to set or query the bandwidth throttling limit. 

This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServerBandwidthProperty</a> on a URL Group or server session.


## -struct-fields




### -field Flags

The <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.


### -field MaxBandwidth

The maximum allowed bandwidth rate in bytesper second. Setting the value to HTTP_LIMIT_INFINITE  allows unlimited bandwidth rate. The value cannot be smaller than HTTP_MIN_ALLOWED_BANDWIDTH_THROTTLING_RATE.


## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

