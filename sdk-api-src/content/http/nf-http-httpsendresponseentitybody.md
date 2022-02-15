---
UID: NF:http.HttpSendResponseEntityBody
title: HttpSendResponseEntityBody function (http.h)
description: Sends entity-body data associated with an HTTP response.
helpviewer_keywords: ["HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA","HTTP_SEND_RESPONSE_FLAG_DISCONNECT","HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING","HTTP_SEND_RESPONSE_FLAG_MORE_DATA","HTTP_SEND_RESPONSE_FLAG_OPAQUE","HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES","HttpSendResponseEntityBody","HttpSendResponseEntityBody function [HTTP]","_http_httpsendresponseentitybody","http.httpsendresponseentitybody","http/HttpSendResponseEntityBody"]
old-location: http\httpsendresponseentitybody.htm
tech.root: http
ms.assetid: f2ff2e40-ef1f-4c35-a615-f31ac63ab738
ms.date: 12/05/2018
ms.keywords: HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA, HTTP_SEND_RESPONSE_FLAG_DISCONNECT, HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING, HTTP_SEND_RESPONSE_FLAG_MORE_DATA, HTTP_SEND_RESPONSE_FLAG_OPAQUE, HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES, HttpSendResponseEntityBody, HttpSendResponseEntityBody function [HTTP], _http_httpsendresponseentitybody, http.httpsendresponseentitybody, http/HttpSendResponseEntityBody
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
 - HttpSendResponseEntityBody
 - http/HttpSendResponseEntityBody
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
 - HttpSendResponseEntityBody
---

# HttpSendResponseEntityBody function


## -description

The 
<b>HttpSendResponseEntityBody</b> function sends entity-body data associated with an HTTP response.

## -parameters

### -param RequestQueueHandle [in]

A handle to the request queue from which the specified request was retrieved. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param RequestId [in]

An identifier of the HTTP request to which this response corresponds. This value is returned in the <b>RequestId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> function. It cannot be <b>HTTP_NULL_ID</b>.

### -param Flags [in]

A parameter that can include  one of the following mutually exclusive flag values.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_DISCONNECT"></a><a id="http_send_response_flag_disconnect"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_DISCONNECT</b></dt>
</dl>
</td>
<td width="60%">
The network connection should be disconnected after sending this response, overriding any persistent connection features associated with the version of HTTP in use. Applications should use this flag to indicate the end of the entity in cases where neither content length nor chunked encoding is used.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_MORE_DATA"></a><a id="http_send_response_flag_more_data"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Additional entity body data for this response is sent by the application through one or more subsequent calls to 
<b>HttpSendResponseEntityBody</b>. The last call then sets this flag to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA"></a><a id="http_send_response_flag_buffer_data"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA</b></dt>
</dl>
</td>
<td width="60%">
This flag enables buffering of data in the kernel on a per-response basis.

It should be used by an application doing synchronous I/O, or by a an application doing asynchronous I/O with no more than one send outstanding at a time.

Applications using asynchronous I/O which may have more than one send outstanding at a time should not use this flag.

When this flag is set, it should be used consistently in calls to the <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> function as well.

<b>Windows Server 2003:  </b>This flag is not supported. This flag is new for Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING"></a><a id="http_send_response_flag_enable_nagling"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING</b></dt>
</dl>
</td>
<td width="60%">
Enables the TCP nagling algorithm for this send only.

<b>Windows Vista and later:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES"></a><a id="http_send_response_flag_process_ranges"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES</b></dt>
</dl>
</td>
<td width="60%">
Specifies that for a range request, the full response content is passed and the caller wants the HTTP API to process ranges appropriately.


<div class="alert"><b>Note</b>  This flag is only supported for responses to HTTP <i>GET</i> requests and offers a limited subset of functionality. Applications that require full range processing should perform it in user mode and not rely on HTTP.sys. It's usage is discouraged.</div>
<div> </div>
Windows Server 2008 R2 and Windows 7 or later.

<b>Note</b>  This flag is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_OPAQUE"></a><a id="http_send_response_flag_opaque"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the request/response is not
HTTP compliant and all subsequent bytes should be treated as entity-body. Applications specify this flag when it is accepting a Web Socket upgrade request and informing HTTP.sys to treat the connection data as opaque data.

This flag is only allowed when the <b>StatusCode</b> member of <i>pHttpResponse</i> is <b>101</b>, switching protocols. <b>HttpSendResponseEntityBody</b> returns <b>ERROR_INVALID_PARAMETER</b> for all other HTTP response types if this flag is used.

<b>Windows 8 and later:  </b>This flag is supported.

</td>
</tr>
</table>
 

<div class="alert"><b>Caution</b>  Combining both flags in a single call to the <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> function produces undefined results.</div>
<div> </div>

### -param EntityChunkCount [in]

A number of structures in the array pointed to by <i>pEntityChunks</i>. This count cannot exceed 9999.

### -param EntityChunks [in]

A pointer to an array of 
<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a> structures to be sent as entity-body data.

### -param BytesSent [out]

Optional. A pointer to a variable that receives the number, in bytes, sent if the function operates synchronously.

When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesSent</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesSent</i> must contain a valid memory address, and not be set to <b>NULL</b>.

### -param Reserved1 [in]

This parameter is reserved and must be <b>NULL</b>.

### -param Reserved2 [in]

This parameter is reserved and must be zero.

### -param Overlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>.

A synchronous call blocks until all response data specified in the <i>pEntityChunks</i> parameter is sent, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

### -param LogData [in, optional]

A pointer to the <a href="/windows/desktop/api/http/ns-http-http_log_data">HTTP_LOG_DATA</a> structure used to log the response. Pass a pointer to the <a href="/windows/desktop/api/http/ns-http-http_log_fields_data">HTTP_LOG_FIELDS_DATA</a> structure and cast it to <b>PHTTP_LOG_DATA</b>.

Be aware that even when logging is enabled on a URL Group, or server session, the response will not be logged unless the application supplies the log fields data structure.

<b>Windows Server 2003 and Windows XP with SP2:  </b>This parameter is reserved and must be <b>NULL</b>.

<b>Windows Vista and Windows Server 2008:  </b>This parameter is new for Windows Vista, and Windows Server 2008

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function is used asynchronously, a return value of <b>ERROR_IO_PENDING</b> indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

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
<dt><b>ERROR_BAD_COMMAND</b></dt>
</dl>
</td>
<td width="60%">
There is a call pending to <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> or <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> having the same <b>RequestId</b>.

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

If neither a Content-length header nor a Transfer-encoding header is included in the response headers, the application must indicate the end of the response by explicitly closing the connection using the <b>HTTP_SEND_RESPONSE_DISCONNECT</b> flag.

<div class="alert"><b>Note</b>  <b>HttpSendResponseEntityBody</b> (or <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>) and <b>HttpSendResponseEntityBody</b> must not be called simultaneously from different threads on the same <i>RequestId</i>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>