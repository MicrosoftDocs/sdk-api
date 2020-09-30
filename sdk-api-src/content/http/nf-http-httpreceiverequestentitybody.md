---
UID: NF:http.HttpReceiveRequestEntityBody
title: HttpReceiveRequestEntityBody function (http.h)
description: Receives additional entity body data for a specified HTTP request.
helpviewer_keywords: ["HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER","HttpReceiveRequestEntityBody","HttpReceiveRequestEntityBody function [HTTP]","_http_httpreceiverequestentitybody","http.httpreceiverequestentitybody","http/HttpReceiveRequestEntityBody"]
old-location: http\httpreceiverequestentitybody.htm
tech.root: http
ms.assetid: b4ba765f-537b-4021-9ecc-d400d9b94723
ms.date: 12/05/2018
ms.keywords: HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER, HttpReceiveRequestEntityBody, HttpReceiveRequestEntityBody function [HTTP], _http_httpreceiverequestentitybody, http.httpreceiverequestentitybody, http/HttpReceiveRequestEntityBody
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
 - HttpReceiveRequestEntityBody
 - http/HttpReceiveRequestEntityBody
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
 - HttpReceiveRequestEntityBody
---

# HttpReceiveRequestEntityBody function


## -description

The 
<b>HttpReceiveRequestEntityBody</b> function receives additional entity body data for a specified HTTP request.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue from which to retrieve the specified entity body data. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param RequestId [in]

The identifier of the HTTP request that contains the retrieved entity body. This value is returned in the <b>RequestId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> function. This value cannot be <b>HTTP_NULL_ID</b>.

### -param Flags [in]

This parameter can be the following flag value. 

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This parameter is reserved and must be zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER"></a><a id="http_receive_request_entity_body_flag_fill_buffer"></a><dl>
<dt><b>HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the buffer will be filled with one or more  entity bodies, unless there are no remaining entity bodies to copy.

</td>
</tr>
</table>

### -param EntityBuffer [out]

A pointer to a buffer that receives entity-body data.

### -param EntityBufferLength [in]

The size, in bytes, of the buffer pointed to by the <i>pBuffer</i> parameter.

### -param BytesReturned [out, optional]

Optional. A pointer to a variables that receives the size, in bytes, of the entity body data returned in the <i>pBuffer</i> buffer. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesReceived</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesReceived</i> must contain a valid memory address, and not be set to <b>NULL</b>.

### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the entity-body data has been retrieved, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function is used asynchronously, a return value of <b>ERROR_IO_PENDING</b> indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

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
One or more of the supplied parameters are in an unusable form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HANDLE_EOF</b></dt>
</dl>
</td>
<td width="60%">
The specified entity body has already been completely retrieved; in this case, the value pointed to by <i>pBytesReceived</i> is not meaningful, and <i>pBuffer</i> should not be examined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DLL_INIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The calling application did not call 
<a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a> before calling this function.

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

To retrieve an entire entity body, an application is expected to call 
<b>HttpReceiveRequestEntityBody</b>, passing in new buffers, until the function returns <b>ERROR_HANDLE_EOF</b>. As long as a buffer full of entity-body data is copied successfully and there is still more entity-body data waiting to be retrieved, the function returns <b>NO_ERROR</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/Http/http-server-sample-application">HTTP Server Sample Application</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>