---
UID: NF:http.HttpWaitForDemandStart
title: HttpWaitForDemandStart function (http.h)
description: Waits for the arrival of a new request that can be served by a new request queue process.
helpviewer_keywords: ["HttpWaitForDemandStart","HttpWaitForDemandStart function [HTTP]","http.httpwaitfordemandstart","http/HttpWaitForDemandStart"]
old-location: http\httpwaitfordemandstart.htm
tech.root: http
ms.assetid: e6bc4d24-5495-44cc-81ee-e5213095f3e4
ms.date: 12/05/2018
ms.keywords: HttpWaitForDemandStart, HttpWaitForDemandStart function [HTTP], http.httpwaitfordemandstart, http/HttpWaitForDemandStart
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
 - HttpWaitForDemandStart
 - http/HttpWaitForDemandStart
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
 - HttpWaitForDemandStart
---

# HttpWaitForDemandStart function


## -description

The <b>HttpWaitForDemandStart</b> function waits for the arrival of a new request that can be served by a new request queue process.

## -parameters

### -param RequestQueueHandle [in]

A handle to the request queue on which demand start is registered. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until a request has arrived in the specified queue, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see  
<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>.

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

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ID_AUTHORITY</b></dt>
</dl>
</td>
<td width="60%">
The calling process is not the controller process for this request queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The calling process has already initiated a shutdown on the request queue or has closed the request queue handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A demand start registration already exists for the request queue.

</td>
</tr>
</table>

## -remarks

Only the controller process can call <b>HttpWaitForDemandStart</b> to register a demand start notification. The controller process is the process that created the request queue and indicated that it is a controller process by passing the <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER</b> flag. If a process other than the controlling process calls <b>HttpWaitForDemandStart</b>, the HTTP Server API returns <b>ERROR_INVALID_ID_AUTHORITY</b>.

<b>HttpWaitForDemandStart</b> completes when a new request arrives for the specified request queue. At this time, a controller process can use this API to start a new worker process to server pending requests. Delayed start of the worker process allows applications to avoid consuming resources until they are required.

The HTTP Server API allows only one outstanding notification registered on a request queue at any time. The HTTP Server API does not enforce limitations on the number of times that <b>HttpWaitForDemandStart</b> can be called on the same request queue consecutively. There is no limit on the number of outstanding processes that are working on the same request queue.

The HTTP Server API supports canceling asynchronous <b>HttpWaitForDemandStart</b> calls. Applications can use <a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a> with the overlapped structure supplied in the <i>pOverlapped</i> parameter, to cancel an outstanding <b>HttpWaitForDemandStart</b> call.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpshutdownrequestqueue">HttpShutdownRequestQueue</a>