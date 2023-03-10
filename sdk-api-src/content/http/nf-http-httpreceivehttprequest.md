---
UID: NF:http.HttpReceiveHttpRequest
title: HttpReceiveHttpRequest function (http.h)
description: Retrieves the next available HTTP request from the specified request queue either synchronously or asynchronously.
helpviewer_keywords: ["0 (zero)","HTTP_RECEIVE_REQUEST_FLAG_COPY_BODY","HTTP_RECEIVE_REQUEST_FLAG_FLUSH_BODY","HttpReceiveHttpRequest","HttpReceiveHttpRequest function [HTTP]","_http_httpreceivehttprequest","http.httpreceivehttprequest","http/HttpReceiveHttpRequest"]
old-location: http\httpreceivehttprequest.htm
tech.root: http
ms.assetid: ad9e80f7-04c4-4108-a7ab-40eb57d00e3b
ms.date: 12/05/2018
ms.keywords: 0 (zero), HTTP_RECEIVE_REQUEST_FLAG_COPY_BODY, HTTP_RECEIVE_REQUEST_FLAG_FLUSH_BODY, HttpReceiveHttpRequest, HttpReceiveHttpRequest function [HTTP], _http_httpreceivehttprequest, http.httpreceivehttprequest, http/HttpReceiveHttpRequest
req.header: http.h
req.include-header: 
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpReceiveHttpRequest
 - http/HttpReceiveHttpRequest
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
 - HttpReceiveHttpRequest
---

# HttpReceiveHttpRequest function


## -description

The 
<b>HttpReceiveHttpRequest</b> function retrieves the next available HTTP request from the specified request queue either synchronously or asynchronously.

## -parameters

### -param RequestQueueHandle [in]

A handle to the request queue from which to retrieve the next available request. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param RequestId [in]

On the first call to retrieve a request, this parameter should be <b>HTTP_NULL_ID</b>. Then, if more than one call is required to retrieve the entire request, 
<b>HttpReceiveHttpRequest</b> or 
<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a> can be called with <i>RequestID</i> set to the value returned in the <b>RequestId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure pointed to by <i>pRequestBuffer</i>.

### -param Flags [in]

A parameter that can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0__zero_"></a><a id="0__ZERO_"></a><dl>
<dt><b>0 (zero)</b></dt>
</dl>
</td>
<td width="60%">
Only the request headers are retrieved; the entity body is not copied.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_RECEIVE_REQUEST_FLAG_COPY_BODY"></a><a id="http_receive_request_flag_copy_body"></a><dl>
<dt><b>HTTP_RECEIVE_REQUEST_FLAG_COPY_BODY</b></dt>
</dl>
</td>
<td width="60%">
The available entity body is copied along with the request headers. The <b>pEntityChunks</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure points to the entity body.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_RECEIVE_REQUEST_FLAG_FLUSH_BODY"></a><a id="http_receive_request_flag_flush_body"></a><dl>
<dt><b>HTTP_RECEIVE_REQUEST_FLAG_FLUSH_BODY</b></dt>
</dl>
</td>
<td width="60%">
All of the entity bodies are copied along with the request headers. The <b>pEntityChunks</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure points to the entity body.

</td>
</tr>
</table>

### -param RequestBuffer [out]

A pointer to a buffer into which the function copies an 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure and entity body for the HTTP request. <b>HTTP_REQUEST.RequestId</b> contains the identifier for this HTTP request, which the application can use in subsequent calls <a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>, 
<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>, or 
<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>.

### -param RequestBufferLength [in]

Size, in bytes, of the  <i>pRequestBuffer</i> buffer.

### -param BytesReturned [out, optional]

Optional. A pointer to a variable that receives the size, in bytes, of the entity body, or of the remaining part of the entity body. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesReceived</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesReceived</i> must contain a valid memory address, and not be set to <b>NULL</b>.

### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until a request has arrived in the specified queue and some or all of it has been retrieved, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see  
<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function is being used asynchronously, a return value of <b>ERROR_IO_PENDING</b> indicates that the next request is not yet ready and will be retrieved later through normal overlapped I/O completion mechanisms.

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
<dt><b>ERROR_NOACCESS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameters points to an invalid or unaligned memory buffer.  The <i>pRequestBuffer</i> parameter must point to a valid memory buffer with a memory alignment equal or greater to the memory alignment requirement for an <b>HTTP_REQUEST</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>RequestBufferLength</i> is greater than or equal to the size of the request header received, but is not as large as the combined size of the request structure and entity body. The buffer size required to read the remaining part of the entity body is returned in the <i>pBytesReceived</i> parameter if this is non-<b>NULL</b> and if the call is synchronous. Call the function again with a large enough buffer to retrieve all data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HANDLE_EOF</b></dt>
</dl>
</td>
<td width="60%">
The specified request has already been completely retrieved; in this case, the value pointed to by <i>pBytesReceived</i> is not meaningful, and <i>pRequestBuffer</i> should not be examined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

</td>
</tr>
</table>

## -remarks

More than one call can be required to retrieve a given request. When the <i>Flags</i> parameter is set to zero, for example, 
<b>HttpReceiveHttpRequest</b> only copies the request header structure into the buffer, and does not attempt to copy any of the entity body. In this case, the 
<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a> function can be used to retrieve the entity body, or a second call can be made to 
<b>HttpReceiveHttpRequest</b>.

Alternatively, the buffer provided by the application may be insufficiently large to receive all or part of the request. To be sure of receiving at least part of the request, it is recommended that an application provide at least a buffer of 4 KB, which accommodates most HTTP requests. Alternately, authentication headers, parsed as unknown headers, can add up to 12 KB to that, so if authentication/authorization is used, a buffer size of at least 16 KB is recommended.

If 
<b>HttpReceiveHttpRequest</b> returns <b>ERROR_MORE_DATA</b>, the application continues to make additional calls, identifying the request in each additional call by passing in the <b>HTTP_REQUEST.RequestId</b> value returned by the first call until <b>ERROR_HANDLE_EOF</b> is returned.

<div class="alert"><b>Note</b>  The application must examine all relevant request headers, including content-negotiation headers if used, and fail the request as appropriate based on the header content. <b>HttpReceiveHttpRequest</b> ensures only that the header line is properly terminated and does not contain illegal characters.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>