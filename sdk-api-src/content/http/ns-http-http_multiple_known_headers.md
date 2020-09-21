---
UID: NS:http._HTTP_MULTIPLE_KNOWN_HEADERS
title: HTTP_MULTIPLE_KNOWN_HEADERS (http.h)
description: Specifies the headers that are included in an HTTP response when more than one header is required.
helpviewer_keywords: ["*PHTTP_MULTIPLE_KNOWN_HEADERS","*PHTTP_MULTIPLE_KNOWN_HEADERS structure [HTTP]","HTTP_MULTIPLE_KNOWN_HEADERS","HTTP_MULTIPLE_KNOWN_HEADERS structure [HTTP]","HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER","http.http_multiple_known_headers","http/*PHTTP_MULTIPLE_KNOWN_HEADERS","http/HTTP_MULTIPLE_KNOWN_HEADERS"]
old-location: http\http_multiple_known_headers.htm
tech.root: http
ms.assetid: b5e68d55-43a4-422f-b7e3-163739628720
ms.date: 12/05/2018
ms.keywords: '*PHTTP_MULTIPLE_KNOWN_HEADERS, *PHTTP_MULTIPLE_KNOWN_HEADERS structure [HTTP], HTTP_MULTIPLE_KNOWN_HEADERS, HTTP_MULTIPLE_KNOWN_HEADERS structure [HTTP], HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER, http.http_multiple_known_headers, http/*PHTTP_MULTIPLE_KNOWN_HEADERS, http/HTTP_MULTIPLE_KNOWN_HEADERS'
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
req.typenames: HTTP_MULTIPLE_KNOWN_HEADERS, *PHTTP_MULTIPLE_KNOWN_HEADERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_MULTIPLE_KNOWN_HEADERS
 - http/_HTTP_MULTIPLE_KNOWN_HEADERS
 - PHTTP_MULTIPLE_KNOWN_HEADERS
 - http/PHTTP_MULTIPLE_KNOWN_HEADERS
 - HTTP_MULTIPLE_KNOWN_HEADERS
 - http/HTTP_MULTIPLE_KNOWN_HEADERS
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
 - HTTP_MULTIPLE_KNOWN_HEADERS
---

# HTTP_MULTIPLE_KNOWN_HEADERS structure


## -description

The <b>HTTP_MULTIPLE_KNOWN_HEADERS</b> structure specifies the headers that are included in an HTTP response when more than one header is required.

## -struct-fields

### -field HeaderId

A member of the <a href="/windows/desktop/api/http/ne-http-http_header_id">HTTP_HEADER_ID</a> enumeration specifying the response header ID.

### -field Flags

The flags corresponding to the response header in the <b>HeaderId</b> member. This member is used only when the WWW-Authenticate header is present. This can be zero or the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER"></a><a id="http_response_info_flags_preserve_order"></a><dl>
<dt><b>HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The specified order of authentication schemes is preserved on the challenge response.

</td>
</tr>
</table>

### -field KnownHeaderCount

The number of elements in  the array specified in the  <b>KnownHeaders</b> member.

### -field KnownHeaders

A pointer to the first element in the array of <a href="/windows/desktop/api/http/ns-http-http_known_header">HTTP_KNOWN_HEADER</a> structures.

## -remarks

The HTTP version 1.0 API allows applications to send only one known response header with the response. Starting with the HTTP version 2.0 API, applications are enabled to send multiple known response headers.

The <b>pInfo</b>  member of the <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structure points to this structure when the application provides multiple known headers on a response. The <b>HTTP_RESPONSE_INFO</b> structure extends the <a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a> structure starting with HTTP version 2.0.

The <b>HTTP_MULTIPLE_KNOWN_HEADERS</b> structure enables server applications to send multiple authentication challenges to the client.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v2">HTTP_RESPONSE_V2</a>