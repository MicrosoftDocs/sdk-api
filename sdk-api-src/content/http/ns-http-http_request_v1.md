---
UID: NS:http._HTTP_REQUEST_V1
title: HTTP_REQUEST_V1 (http.h)
description: Uses the HTTP_REQUEST structure to return data associated with a specific request.
helpviewer_keywords: ["*PHTTP_REQUEST","*PHTTP_REQUEST_V1","HTTP_REQUEST","HTTP_REQUEST_FLAG_HTTP2","HTTP_REQUEST_FLAG_MORE_ENTITY_BODY_EXISTS","HTTP_REQUEST_FLAG_IP_ROUTED","HTTP_REQUEST_V1","HTTP_REQUEST_V1 structure [HTTP]","PHTTP_REQUEST_V1","PHTTP_REQUEST_V1 structure pointer [HTTP]","http.http_request_v1","http/HTTP_REQUEST_V1","http/PHTTP_REQUEST_V1"]
old-location: http\http_request_v1.htm
tech.root: http
ms.assetid: 5550c49c-36ef-42e6-8134-5d9d0d9d53b5
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST, *PHTTP_REQUEST_V1, HTTP_REQUEST, HTTP_REQUEST_FLAG_HTTP2, HTTP_REQUEST_FLAG_MORE_ENTITY_BODY_EXISTS, HTTP_REQUEST_FLAG_IP_ROUTED, HTTP_REQUEST_V1, HTTP_REQUEST_V1 structure [HTTP], PHTTP_REQUEST_V1, PHTTP_REQUEST_V1 structure pointer [HTTP], http.http_request_v1, http/HTTP_REQUEST_V1, http/PHTTP_REQUEST_V1'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HTTP_REQUEST_V1, *PHTTP_REQUEST_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_V1
 - http/_HTTP_REQUEST_V1
 - PHTTP_REQUEST_V1
 - http/PHTTP_REQUEST_V1
 - HTTP_REQUEST_V1
 - http/HTTP_REQUEST_V1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_REQUEST_V1
---

## -description

Uses the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure to return data associated with a specific request.

Do not use <b>HTTP_REQUEST_V1</b> directly in your code; using <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> instead ensures that the proper version, based on the operating system the code is compiled under, is used.

## -struct-fields

### -field Flags

A combination of zero or more of the following flag values may be combined, with OR, as appropriate.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_REQUEST_FLAG_MORE_ENTITY_BODY_EXISTS"></a><a id="http_request_flag_more_entity_body_exists"></a><dl>
<dt><b>HTTP_REQUEST_FLAG_MORE_ENTITY_BODY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
There is more entity body to be read for this request. This applies only to incoming requests that span multiple reads. 

If this value is not set, either the whole entity body was copied into the buffer specified by <b>pEntityChunks</b> or the request did not include an entity body.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_REQUEST_FLAG_IP_ROUTED"></a><a id="http_request_ip_routed"></a><dl>
<dt><b>HTTP_REQUEST_FLAG_IP_ROUTED</b></dt>
</dl>
</td>
<td width="60%">
The request was routed based on host and IP binding. The application should  reflect the local IP while flushing kernel
 cache entries for this request.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_REQUEST_FLAG_HTTP2"></a><a id="http_request_flag_http2"></a><dl>
<dt><b>HTTP_REQUEST_FLAG_HTTP2</b></dt>
</dl>
</td>
<td width="60%">
Indicates the request was received over HTTP/2.

</td>
</tr>
</table>

### -field ConnectionId

An identifier for the connection on which the request was received. Use this value when calling 
<a href="/windows/desktop/api/http/nf-http-httpwaitfordisconnect">HttpWaitForDisconnect</a> or 
<a href="/windows/desktop/api/http/nf-http-httpreceiveclientcertificate">HttpReceiveClientCertificate</a>.

### -field RequestId

A value used to identify the request when calling 
<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>, 
<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>, and/or 
<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>.

### -field UrlContext

The context that is associated with the URL in the <i>pRawUrl</i> parameter.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>

### -field Version

An 
<a href="/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure that contains the version of HTTP specified by this request.

### -field Verb

An HTTP verb associated with this request. This member can be one of the values from the  
<a href="/windows/desktop/api/http/ne-http-http_verb">HTTP_VERB</a> enumeration.

### -field UnknownVerbLength

If the <b>Verb</b> member contains a value equal to <b>HttpVerbUnknown</b>, the <b>UnknownVerbLength</b> member contains the size, in bytes, of the string pointed to by the <b>pUnknownVerb</b> member, not including the terminating null character. If <b>Verb</b> is not equal to <b>HttpVerbUnknown</b>, <b>UnknownVerbLength</b> is equal to zero.

### -field RawUrlLength

The size, in bytes, of the unprocessed URL string pointed to by the <b>pRawUrl</b> member, not including the terminating null character.

### -field pUnknownVerb

If the <b>Verb</b> member is equal to <b>HttpVerbUnknown</b>, <b>pUnknownVerb</b>, points to a null-terminated string of octets that contains the HTTP verb for this request; otherwise, the application ignores this parameter.

### -field pRawUrl

A pointer to a string of octets that contains the original, unprocessed URL targeted by this request.  Use this unprocessed URL only for tracking or statistical purposes; the  <b>CookedUrl</b> member contains the canonical form of the URL for general use.

### -field CookedUrl

An 
<a href="/windows/desktop/api/http/ns-http-http_cooked_url">HTTP_COOKED_URL</a> structure that contains a parsed canonical wide-character version of the URL targeted by this request. This is the version of the URL HTTP Listeners should act upon, rather than the raw URL.

### -field Address

An 
<a href="/windows/desktop/api/http/ns-http-http_transport_address">HTTP_TRANSPORT_ADDRESS</a> structure that contains the transport addresses for the connection for this request.

### -field Headers

An 
<a href="/windows/desktop/api/http/ns-http-http_request_headers">HTTP_REQUEST_HEADERS</a> structure that contains the headers specified in this request.

### -field BytesReceived

The total number of bytes received from the network comprising this request.

### -field EntityChunkCount

The number of elements in the <b>pEntityChunks</b> array. If no entity body was copied, this value is zero.

### -field pEntityChunks

A pointer to an array of 
<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a> structures that contains the data blocks making up the entity body. 
<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> does not copy the entity body unless called with the HTTP_RECEIVE_REQUEST_FLAG_COPY_BODY flag set.

### -field RawConnectionId

Raw connection ID for an Secure Sockets Layer (SSL) request.

### -field pSslInfo

A pointer to an 
<a href="/windows/desktop/api/http/ns-http-http_ssl_info">HTTP_SSL_INFO</a> structure that contains Secure Sockets Layer (SSL) information about the connection on which the request was received.

## -remarks

The unprocessed URL contained in the <b>pRawUrl</b> member is for tracking and statistical purposes only. For other purposes, use the processed, canonical URL contained in the <b>CookedUrl</b> member.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_cooked_url">HTTP_COOKED_URL</a>



<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/api/http/ns-http-http_request_v2">HTTP_REQUEST_V2</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_ssl_info">HTTP_SSL_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_transport_address">HTTP_TRANSPORT_ADDRESS</a>



<a href="/windows/desktop/api/http/ne-http-http_verb">HTTP_VERB</a>



<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>