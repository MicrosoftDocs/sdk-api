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

# HttpInitialize function


## -description


The 
<b>HttpInitialize</b> function initializes the HTTP Server API driver, starts it, if it has not already been started, and allocates data structures for the calling application to support response-queue creation and other operations. Call this function before calling any other functions in the HTTP Server API.


## -parameters




### -param Version [in]

HTTP version. This parameter is an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure. For the current version, declare an instance of the structure and set it to the pre-defined value HTTPAPI_VERSION_1 before passing it to 
<b>HttpInitialize</b>.


### -param Flags [in]

Initialization options, which can include one or both of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_INITIALIZE_CONFIG"></a><a id="http_initialize_config"></a><dl>
<dt><b>HTTP_INITIALIZE_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
Perform initialization for applications that use the HTTP configuration functions, 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>, 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> and 
<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_INITIALIZE_SERVER"></a><a id="http_initialize_server"></a><dl>
<dt><b>HTTP_INITIALIZE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Perform initialization for applications that use the HTTP Server API.

</td>
</tr>
</table>
 


### -param pReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Flags</i> parameter contains an unsupported value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -remarks



Call 
<a href="https://msdn.microsoft.com/d1922375-3d59-45a7-9d1d-08dbce1111ff">HttpTerminate</a> when the application completes. All the same flags that were passed to 
<b>HttpInitialize</b> in the <i>Flags</i> parameter must also be passed to 
<b>HttpTerminate</b>. An application can call 
<b>HttpInitialize</b> repeatedly, provided that each call to 
<b>HttpInitialize</b> is later matched by a corresponding call to 
<b>HttpTerminate</b>.




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/d1922375-3d59-45a7-9d1d-08dbce1111ff">HttpTerminate</a>
 

 

