---
UID: NF:http.HttpSendHttpResponse
title: HttpSendHttpResponse function (http.h)
description: Sends an HTTP response to the specified HTTP request.
helpviewer_keywords: ["HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA","HTTP_SEND_RESPONSE_FLAG_DISCONNECT","HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING","HTTP_SEND_RESPONSE_FLAG_MORE_DATA","HTTP_SEND_RESPONSE_FLAG_OPAQUE","HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES","HttpSendHttpResponse","HttpSendHttpResponse function [HTTP]","_http_httpsendhttpresponse","http.httpsendhttpresponse","http/HttpSendHttpResponse"]
old-location: http\httpsendhttpresponse.htm
tech.root: http
ms.assetid: 0183584f-105e-4fa3-8991-d3f2dfca1d62
ms.date: 12/05/2018
ms.keywords: HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA, HTTP_SEND_RESPONSE_FLAG_DISCONNECT, HTTP_SEND_RESPONSE_FLAG_ENABLE_NAGLING, HTTP_SEND_RESPONSE_FLAG_MORE_DATA, HTTP_SEND_RESPONSE_FLAG_OPAQUE, HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES, HttpSendHttpResponse, HttpSendHttpResponse function [HTTP], _http_httpsendhttpresponse, http.httpsendhttpresponse, http/HttpSendHttpResponse
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
 - HttpSendHttpResponse
 - http/HttpSendHttpResponse
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
 - HttpSendHttpResponse
---

# HttpSendHttpResponse function


## -description

The 
<b>HttpSendHttpResponse</b> function sends an HTTP response to the specified HTTP request.

## -parameters

### -param RequestQueueHandle [in]

A handle to the request queue from which the specified request was retrieved. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param RequestId [in]

An identifier of the HTTP request to which this response corresponds. This value is returned in the <b>RequestId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> function. This value cannot be <b>HTTP_NULL_ID</b>.

### -param Flags [in]

This parameter can be a combination of some of the following flag values.  Those that are mutually exclusive are marked accordingly.

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
The network connection should be disconnected after sending this response, overriding any persistent connection features associated with the version of HTTP in use.<div class="alert"><b>Caution</b>  Combining <b>HTTP_SEND_RESPONSE_FLAG_DISCONNECT</b> and <b>HTTP_SEND_RESPONSE_FLAG_MORE_DATA</b> in a single call to the <b>HttpSendHttpResponse</b> function produces undefined results.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_MORE_DATA"></a><a id="http_send_response_flag_more_data"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Additional entity body data for this response is sent by the application through one or more subsequent calls to 
<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>. The last call sending entity-body data then sets this flag to zero.

<div class="alert"><b>Caution</b>  Combining <b>HTTP_SEND_RESPONSE_FLAG_DISCONNECT</b> and <b>HTTP_SEND_RESPONSE_FLAG_MORE_DATA</b> in a single call to the <b>HttpSendHttpResponse</b> function produces undefined results.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA"></a><a id="http_send_response_flag_buffer_data"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_BUFFER_DATA</b></dt>
</dl>
</td>
<td width="60%">
This flag enables buffering of data in the kernel on a per-response basis.

It should be used by an application doing synchronous I/O or by an application doing asynchronous I/O with no more than one outstanding send at a time.

Applications that use asynchronous I/O and that may have more than one send outstanding at a time should not use this flag.

When this flag is set, it should also be used consistently in calls to the <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> function.

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

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES"></a><a id="http_send_response_flag_process_ranges"></a><dl>
<dt><b>HTTP_SEND_RESPONSE_FLAG_PROCESS_RANGES</b></dt>
</dl>
</td>
<td width="60%">
Specifies that for a range request, the full response content is passed and the caller wants the HTTP API to process ranges appropriately.


<div class="alert"><b>Note</b>  This flag is only supported for responses to HTTP <i>GET</i> requests and offers a limited subset of functionality. Applications that require full range processing should perform it in user mode and not rely on HTTP.sys. Its usage is discouraged.</div>
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

This flag is only allowed when the <b>StatusCode</b> member of <i>pHttpResponse</i> is <b>101</b>, switching protocols. <b>HttpSendHttpResponse</b> returns <b>ERROR_INVALID_PARAMETER</b> for all other HTTP response types if this flag is used.

<b>Windows 8 and later:  </b>This flag is supported.

</td>
</tr>
</table>

### -param HttpResponse [in]

A pointer to an 
<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a> structure that defines the HTTP response.

### -param CachePolicy [in, optional]

A pointer to the <a href="/windows/desktop/api/http/ns-http-http_cache_policy">HTTP_CACHE_POLICY</a> structure used to cache the response.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This parameter is reserved and must be <b>NULL</b>.

### -param BytesSent [out]

Optional. A pointer to a variable that receives the number, in bytes, sent if the function operates synchronously.

When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesSent</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesSent</i> must contain a valid memory address and not be set to <b>NULL</b>.

### -param Reserved1 [in]

This parameter is reserved and must be <b>NULL</b>.

### -param Reserved2 [in]

This parameter is reserved and must be zero.

### -param Overlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set  to <b>NULL</b>.

A synchronous call blocks until all response data specified in the <i>pHttpResponse</i> parameter is sent, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

### -param LogData [in, optional]

A pointer to the  <a href="/windows/desktop/api/http/ns-http-http_log_data">HTTP_LOG_DATA</a> structure used to log the response. Pass a pointer to the <a href="/windows/desktop/api/http/ns-http-http_log_fields_data">HTTP_LOG_FIELDS_DATA</a> structure and cast it to <b>PHTTP_LOG_DATA</b>.

Be aware that even when logging is enabled on a URL Group, or server session, the response will not be logged unless the application supplies the log fields data structure.

<b>Windows Server 2003 and Windows XP with SP2:  </b>This parameter is reserved and must be <b>NULL</b>.

<b>Windows Vista and Windows Server 2008:  </b>This parameter is new for Windows Vista, and Windows Server 2008

## -returns

If the function succeeds, the function returns <b>NO_ERROR</b>.

If the function is used asynchronously, a return value of <b>ERROR_IO_PENDING</b> indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

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
A <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

</td>
</tr>
</table>

## -remarks

The 
<b>HttpSendHttpResponse</b> function is used to create and send a response header, and the 
<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> function can be used to send entity-body data as required.

If neither a content-length header nor a transfer-encoding header is included with the response, the application must indicate the end of the response by explicitly closing the connection by using the <b>HTTP_SEND_RESPONSE_DISCONNECT</b> flag.

 If an application specifies a "Server:" header in a response,  using the <b>HttpHeaderServer</b> identifier in the <a href="/windows/desktop/api/http/ns-http-http_known_header">HTTP_KNOWN_HEADER</a> structure, that specified value is placed as the first part of the header, followed by a space and then "Microsoft-HTTPAPI/1.0". If no server header is specified, <b>HttpSendHttpResponse</b> supplies "Microsoft-HTTPAPI/1.0" as the server header.

<div class="alert"><b>Note</b>  The <b>HttpSendHttpResponse</b> and <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> function must not be called simultaneously from different threads on the same <i>RequestId</i>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>
