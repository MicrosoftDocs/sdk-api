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

# _XHR_PROPERTY enumeration


## -description


Defines properties that you can assign to an outgoing HTTP request by calling the <a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a> method.


## -enum-fields




### -field XHR_PROP_NO_CRED_PROMPT

Sets a flag in the HTTP request that suppresses automatic prompts for credentials.


### -field XHR_PROP_NO_AUTH

Sets a flag in the HTTP request that configures the HTTP request that disables authentication for the request.


### -field XHR_PROP_TIMEOUT

Sets the connect, send, and receive timeouts for HTTP socket operations.

<div class="alert"><b>Note</b>  This value will not affect the timeout behavior of the entire request process.</div>
<div> </div>

### -field XHR_PROP_NO_DEFAULT_HEADERS

Suppresses adding default headers to the HTTP request.


### -field XHR_PROP_REPORT_REDIRECT_STATUS

Causes the HTTP stack to call the <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> callback method with an interim redirecting status code.  The <b>OnHeadersAvailable</b> will be called again for additional redirects and the final destination status code.


### -field XHR_PROP_NO_CACHE

Suppresses cache reads and writes for the HTTP request.


### -field XHR_PROP_EXTENDED_ERROR

Causes the HTTP stack to provide <b>HRESULTS</b> with the underlying Win32 error code to the <a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a> callback method in case of failure.


### -field XHR_PROP_QUERY_STRING_UTF8

Causes the query string to be encoded in UTF8 instead of ACP for HTTP request.


### -field XHR_PROP_IGNORE_CERT_ERRORS

Suppresses certain certificate errors.


### -field XHR_PROP_ONDATA_THRESHOLD


### -field XHR_PROP_SET_ENTERPRISEID


### -field XHR_PROP_MAX_CONNECTIONS




## -see-also




<a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

