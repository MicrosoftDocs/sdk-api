---
UID: NE:http._HTTP_SERVICE_CONFIG_TIMEOUT_KEY
title: "_HTTP_SERVICE_CONFIG_TIMEOUT_KEY"
author: windows-sdk-content
description: The HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration defines the type of timer that is queried or configured through the HTTP_SERVICE_CONFIG_TIMEOUT_SET structure.
old-location: http\http_service_config_timeout_key.htm
tech.root: Http
ms.assetid: e591a6b8-e63f-40c3-bd48-e14cb9f89453
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY, *PHTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP], HTTP_SERVICE_CONFIG_TIMEOUT_KEY, HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration [HTTP], HeaderWaitTimeout, IdleConnectionTimeout, _HTTP_SERVICE_CONFIG_TIMEOUT_KEY, http.http_service_config_timeout_key, http/*PHTTP_SERVICE_CONFIG_TIMEOUT_KEY, http/HTTP_SERVICE_CONFIG_TIMEOUT_KEY, http/HeaderWaitTimeout, http/IdleConnectionTimeout"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - HTTP_SERVICE_CONFIG_TIMEOUT_KEY
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_CONFIG_TIMEOUT_KEY, *PHTTP_SERVICE_CONFIG_TIMEOUT_KEY
req.redist: 
---

# _HTTP_SERVICE_CONFIG_TIMEOUT_KEY enumeration


## -description


The <b>HTTP_SERVICE_CONFIG_TIMEOUT_KEY</b> enumeration defines the type of timer that is queried or configured through the <a href="https://msdn.microsoft.com/928cb09d-9f63-4334-b034-ee27e950ce0a">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a> structure.


## -enum-fields




### -field IdleConnectionTimeout

The maximum time allowed for a connection to remain idle, after which, the connection is timed out and reset.


### -field HeaderWaitTimeout

The maximum time allowed to parse all the request headers, including the request line, after which, the connection is timed out and reset.


## -remarks



 The <b>HTTP_SERVICE_CONFIG_TIMEOUT_KEY</b> enumeration is used in the <a href="https://msdn.microsoft.com/928cb09d-9f63-4334-b034-ee27e950ce0a">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a> structure to define the type of timer that is configured. The <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure passes data to  the <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a> function through  the <i>pConfigInformation</i> parameter or retrieves data from the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is equal to <b>HttpServiceConfigTimeout</b>.




## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/928cb09d-9f63-4334-b034-ee27e950ce0a">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a>
 

 

