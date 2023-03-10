---
UID: NF:http.HttpShutdownRequestQueue
title: HttpShutdownRequestQueue function (http.h)
description: Stops queuing requests for the specified request queue process.
helpviewer_keywords: ["HttpShutdownRequestQueue","HttpShutdownRequestQueue function [HTTP]","http.httpshutdownrequestqueue","http/HttpShutdownRequestQueue"]
old-location: http\httpshutdownrequestqueue.htm
tech.root: http
ms.assetid: f6640565-a5a1-4a71-938c-1adf54beb40a
ms.date: 12/05/2018
ms.keywords: HttpShutdownRequestQueue, HttpShutdownRequestQueue function [HTTP], http.httpshutdownrequestqueue, http/HttpShutdownRequestQueue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpShutdownRequestQueue
 - http/HttpShutdownRequestQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpShutdownRequestQueue
---

# HttpShutdownRequestQueue function


## -description

The <b>HttpShutdownRequestQueue</b> function stops queuing requests for the specified request queue process. Outstanding calls to <a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> are canceled.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue that is shut down. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

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
<li>If the calling process is a controller, outstanding <a href="/windows/desktop/api/http/nf-http-httpwaitfordemandstart">HttpWaitForDemandStart</a> calls are canceled.</li>
<li>Pending <a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> calls from the calling process are canceled.</li>
<li>Requests that are already bound to the calling process are canceled.</li>
<li>The unreceived pending requests that are queued to the request queue process rerouted to another  request queue process. If no other request queue process is available, the pending requests are saved until the request queue is closed, or another non-controller request queue process launches.</li>
<li>Pending <a href="/windows/desktop/api/http/nf-http-httpwaitfordisconnect">HttpWaitForDisconnect</a> calls initiated by the calling process are canceled.</li>
<li>Outstanding responses indicated by the calling process are not affected, they are properly completed.</li>
</ol>


Be aware that if the request queue handle is shared by multiple processes,  <b>HttpShutdownRequestQueue</b> limits cleanup to the calling process. Other processes currently working on the request queue are not affected.

<b>HttpShutdownRequestQueue</b> can be used by applications to recycle request queue processes. For this purpose, <b>HttpShutdownRequestQueue</b> is called prior to terminating a process that shares the request queue with other processes. After <b>HttpShutdownRequestQueue</b>  returns, the process can be safely terminated or recycled.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>