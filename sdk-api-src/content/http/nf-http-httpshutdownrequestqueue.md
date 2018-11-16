---
UID: NF:http.HttpShutdownRequestQueue
title: HttpShutdownRequestQueue function
author: windows-sdk-content
description: Stops queuing requests for the specified request queue process.
old-location: http\httpshutdownrequestqueue.htm
tech.root: Http
ms.assetid: f6640565-a5a1-4a71-938c-1adf54beb40a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HttpShutdownRequestQueue, HttpShutdownRequestQueue function [HTTP], http.httpshutdownrequestqueue, http/HttpShutdownRequestQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpShutdownRequestQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- HttpShutdownRequestQueue
: 
---

# HttpShutdownRequestQueue function


## -description


The <b>HttpShutdownRequestQueue</b> function stops queuing requests for the specified request queue process. Outstanding calls to <a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a> are canceled.


## -parameters




### -param RequestQueueHandle [in]

The handle to the request queue that is shut down. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>

If the function fails, it returns one of the following error codes.

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
The <i>ReqQueueHandle</i> parameter does not contain a valid request queue.

The application does not have permission to shut down the request queue.

</td>
</tr>
</table>
 




## -remarks



<b>HttpShutdownRequestQueue</b> cancels outstanding requests and stops all processing on the request queue process. The following steps are performed when this function is called:


<ol>
<li>The request queue process is marked  for cleanup and no new requests are routed to the request queue process.</li>
<li>If the calling process is a controller, outstanding <a href="https://msdn.microsoft.com/e6bc4d24-5495-44cc-81ee-e5213095f3e4">HttpWaitForDemandStart</a> calls are canceled.</li>
<li>Pending <a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a> calls from the calling process are canceled.</li>
<li>Requests that are already bound to the calling process are canceled.</li>
<li>The unreceived pending requests that are queued to the request queue process rerouted to another  request queue process. If no other request queue process is available, the pending requests are saved until the request queue is closed, or another non-controller request queue process launches.</li>
<li>Pending <a href="https://msdn.microsoft.com/1f1c16c1-43ef-4e29-8d3d-8592ce6a6bf0">HttpWaitForDisconnect</a> calls initiated by the calling process are canceled.</li>
<li>Outstanding responses indicated by the calling process are not affected, they are properly completed.</li>
</ol>


Be aware that if the request queue handle is shared by multiple processes,  <b>HttpShutdownRequestQueue</b> limits cleanup to the calling process. Other processes currently working on the request queue are not affected.

<b>HttpShutdownRequestQueue</b> can be used by applications to recycle request queue processes. For this purpose, <b>HttpShutdownRequestQueue</b> is called prior to terminating a process that shares the request queue with other processes. After <b>HttpShutdownRequestQueue</b>  returns, the process can be safely terminated or recycled.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/dfbc2d32-c1f6-41b1-8f4f-9e5e9f6dd9e1">HttpCloseRequestQueue</a>



<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>



<a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>
 

 

