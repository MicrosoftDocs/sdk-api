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
 

 

