---
UID: NS:http._HTTP_LOG_FIELDS_DATA
title: HTTP_LOG_FIELDS_DATA (http.h)
description: Used to pass the fields that are logged for an HTTP response when WC3 logging is enabled.
helpviewer_keywords: ["*PHTTP_LOG_FIELDS_DATA","*PHTTP_LOG_FIELDS_DATA structure [HTTP]","HTTP_LOG_FIELDS_DATA","HTTP_LOG_FIELDS_DATA structure [HTTP]","http.http_log_fields_data","http/*PHTTP_LOG_FIELDS_DATA","http/HTTP_LOG_FIELDS_DATA"]
old-location: http\http_log_fields_data.htm
tech.root: http
ms.assetid: 5d1b86fe-161d-4182-b3fe-9a03a843e62e
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LOG_FIELDS_DATA, *PHTTP_LOG_FIELDS_DATA structure [HTTP], HTTP_LOG_FIELDS_DATA, HTTP_LOG_FIELDS_DATA structure [HTTP], http.http_log_fields_data, http/*PHTTP_LOG_FIELDS_DATA, http/HTTP_LOG_FIELDS_DATA'
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
req.typenames: HTTP_LOG_FIELDS_DATA, *PHTTP_LOG_FIELDS_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LOG_FIELDS_DATA
 - http/_HTTP_LOG_FIELDS_DATA
 - PHTTP_LOG_FIELDS_DATA
 - http/PHTTP_LOG_FIELDS_DATA
 - HTTP_LOG_FIELDS_DATA
 - http/HTTP_LOG_FIELDS_DATA
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
 - HTTP_LOG_FIELDS_DATA
---

# HTTP_LOG_FIELDS_DATA structure


## -description

The <b>HTTP_LOG_FIELDS_DATA</b> structure is used to pass the fields that are logged for an HTTP response when WC3 logging is enabled.

## -struct-fields

### -field Base

Initialize this member to the <b>HttpLogDataTypeFields</b> value of the <a href="/windows/desktop/api/http/ne-http-http_log_data_type">HTTP_LOG_DATA_TYPE</a> enumeration.

### -field UserNameLength

The size, in bytes, of the user name member.

### -field UriStemLength

The size, in bytes, of the URI stem member.

### -field ClientIpLength

The size, in bytes, of the client IP address member.

### -field ServerNameLength

The size, in bytes, of the server name member.

### -field ServiceNameLength

### -field ServerIpLength

The size, in bytes, of the server IP address member.

### -field MethodLength

The size, in bytes, of the HTTP method member.

### -field UriQueryLength

The size, in bytes, of the URI query member.

### -field HostLength

The size, in bytes, of the host name member.

### -field UserAgentLength

The size, in bytes, of the user agent member.

### -field CookieLength

The size, in bytes, of the cookie member.

### -field ReferrerLength

The size, in bytes, of the referrer member.

### -field UserName

The name of the  user.

### -field UriStem

The URI stem.

### -field ClientIp

The IP address of the client.

### -field ServerName

The name of the server.

### -field ServiceName

The name of the service.

### -field ServerIp

The IP address of the server.

### -field Method

The HTTP method.

### -field UriQuery

The URI query.

### -field Host

The host information from the request.

### -field UserAgent

The user agent name.

### -field Cookie

The cookie provided by the application.

### -field Referrer

The referrer.

### -field ServerPort

The port for the server.

### -field ProtocolStatus

The protocol status.

### -field Win32Status

The win32 status.

### -field MethodNum

The method number.

### -field SubStatus

The sub status.

## -remarks

The <b>HTTP_LOG_FIELDS_DATA</b> structure is an optional parameter (pLogData) in the <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> and <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> functions starting with the HTTP version 2.0 API. The <b>HTTP_LOG_FIELDS_DATA</b> structure specifies which fields are logged in the response.

Unless this structure is passed, the response will not be logged, even when the server logging property is set on a URL group or  a server session. Requests will not be logged unless the application passes the <b>HTTP_LOG_FIELDS_DATA</b> structure with each response and the logging property is set on the server session or URL Group. Most of the fields in the <b>HTTP_LOG_FIELDS_DATA</b> structure can be initialized from the corresponding field in the <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure, however, some of the log fields are only known to the application; for example, Win32Status and SubStatus. This structure enables applications to alter the fields that are logged. The application passes a <b>NULL</b> pointer and a zero length for the corresponding member to disable logging for that field.

 Applications must provide the <b>HTTP_LOG_FIELDS_DATA</b> structure with the last send call.  If a response is sent with a single call to <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>, the log data must be provided in this call. If the response is sent over multiple send calls, the data must be provided with the last call to <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v1">HTTP_RESPONSE_V1</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v2">HTTP_RESPONSE_V2</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>