---
UID: NF:http.HttpWaitForDisconnect
title: HttpWaitForDisconnect function
author: windows-sdk-content
description: Notifies the application when the connection to an HTTP client is broken for any reason.
old-location: http\httpwaitfordisconnect.htm
old-project: http
ms.assetid: 1f1c16c1-43ef-4e29-8d3d-8592ce6a6bf0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpWaitForDisconnect, HttpWaitForDisconnect function [HTTP], _http_httpwaitfordisconnect, http.httpwaitfordisconnect, http/HttpWaitForDisconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: http.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpWaitForDisconnect
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpWaitForDisconnect function


## -description


The 
<b>HttpWaitForDisconnect</b> function notifies the application when the connection to an HTTP client is broken for any reason.


## -parameters




### -param RequestQueueHandle [in]

A handle to the request queue that handles requests from the specified connection. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param ConnectionId [in]

Identifier for the connection to the client computer. This value is returned in the <b>ConnectionID</b> member of the 
<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure by a call to the 
<a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a> function.


### -param OPTIONAL

TBD




#### - pOverlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the connection is broken, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For information about using 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structures for synchronization, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function is used asynchronously, a return value of ERROR_IO_PENDING indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

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
One or more of the supplied parameters is in an unusable form.

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
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>
 

 

