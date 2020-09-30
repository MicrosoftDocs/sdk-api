---
UID: NS:http._HTTP_TIMEOUT_LIMIT_INFO
title: HTTP_TIMEOUT_LIMIT_INFO (http.h)
description: Defines the application-specific connection timeout limits.
helpviewer_keywords: ["*PHTTP_TIMEOUT_LIMIT_INFO","*PHTTP_TIMEOUT_LIMIT_INFO structure [HTTP]","HTTP_TIMEOUT_LIMIT_INFO","HTTP_TIMEOUT_LIMIT_INFO structure [HTTP]","http.http_timeout_limit_info","http/*PHTTP_TIMEOUT_LIMIT_INFO","http/HTTP_TIMEOUT_LIMIT_INFO"]
old-location: http\http_timeout_limit_info.htm
tech.root: http
ms.assetid: 900f4b4d-c34d-4994-b8eb-b3f15e54f29a
ms.date: 12/05/2018
ms.keywords: '*PHTTP_TIMEOUT_LIMIT_INFO, *PHTTP_TIMEOUT_LIMIT_INFO structure [HTTP], HTTP_TIMEOUT_LIMIT_INFO, HTTP_TIMEOUT_LIMIT_INFO structure [HTTP], http.http_timeout_limit_info, http/*PHTTP_TIMEOUT_LIMIT_INFO, http/HTTP_TIMEOUT_LIMIT_INFO'
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
req.typenames: HTTP_TIMEOUT_LIMIT_INFO, *PHTTP_TIMEOUT_LIMIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_TIMEOUT_LIMIT_INFO
 - http/_HTTP_TIMEOUT_LIMIT_INFO
 - PHTTP_TIMEOUT_LIMIT_INFO
 - http/PHTTP_TIMEOUT_LIMIT_INFO
 - HTTP_TIMEOUT_LIMIT_INFO
 - http/HTTP_TIMEOUT_LIMIT_INFO
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
 - HTTP_TIMEOUT_LIMIT_INFO
---

# HTTP_TIMEOUT_LIMIT_INFO structure


## -description

The <b>HTTP_TIMEOUT_LIMIT_INFO</b> structure defines the application-specific connection timeout limits.

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerTimeoutsProperty</a> on a URL Group, server session,  or request queue.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure that specifies whether the property is present.

### -field EntityBody

The time, in seconds, allowed for the request entity body to arrive.

 The HTTP Server API turns on this timer when the request has an entity body. The timer expiration is initially set to the configured value. When the  HTTP Server API receives additional data indications on the request, it resets the timer to give the connection another interval.

### -field DrainEntityBody

The time, in seconds, allowed for the HTTP Server API to drain the entity body on a Keep-Alive connection.

On a Keep-Alive connection, after the application has sent a response for a request and before the request entity body has completely arrived, the HTTP Server API starts draining the remainder of the entity body to reach another potentially pipelined request from the client. If the time to drain the remaining entity body exceeds the allowed period the connection is timed out.

### -field RequestQueue

The time, in seconds, allowed  for the request to remain in the request queue before the application picks it up.

### -field IdleConnection

The time, in seconds, allowed for an idle connection.

This timeout is only enforced after the first request on the connection is routed to the application. For more information, see the Remarks section.

### -field HeaderWait

The time, in seconds, allowed for the HTTP Server API to  parse the request header.

This timeout is only enforced after the first request on the connection is routed to the application. For more information, see the Remarks section.

### -field MinSendRate

The minimum send rate, in bytes-per-second, for the response. The default response send rate is 150 bytes-per-second.

To disable this timer, set <b>MinSendRate</b> to <b>MAXULONG</b>.

## -remarks

This structure is used in the <a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>, and  <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a> functions to set or query the connection timeouts. The following table lists the default timeouts.

<table>
<tr>
<th>Timer</th>
<th>HTTP Server API Default</th>
<th>HTTP Server API  Wide Configuration</th>
<th>Application Specific Configuration</th>
</tr>
<tr>
<td>EntityBody</td>
<td>2 Minutes</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td> DrainEntityBody</td>
<td>2 Minutes</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td>RequestQueue</td>
<td>2 Minutes</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td>IdleConnection</td>
<td>2 Minutes</td>
<td>Yes</td>
<td>Limited</td>
</tr>
<tr>
<td>HeaderWait</td>
<td>2 Minutes</td>
<td>Yes</td>
<td>Limited</td>
</tr>
<tr>
<td>MinSendRate</td>
<td>150 bytes/second</td>
<td>No</td>
<td>Yes</td>
</tr>
</table>
 

Calling <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a> or <a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a> to configure a connection timeout affects only the calling application and does not set driver wide timeout limits. The idle connection and header wait timers can be configured for all HTTP applications by calling <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>. Administrative privileges are required to configure HTTP Server API wide timeouts. HTTP Server API wide configurations affect all HTTP applications on the computer and persist when the computer is shut down.

The application-specific <b>IdleConnection</b>  and <b>HeaderWait</b> timers are set on a limited basis. The HTTP Server API cannot determine the request queue or URL group that the request is associated with until the headers have been parsed. Therefore, the HTTP Server API enforces the default <b>IdleConnection</b>  and <b>HeaderWait</b> timers for the first request on a connection.  Subsequent requests on a Keep-Alive connection will use the application specific timeouts.

Setting a timeout on a server session affects all the URL Groups under the server session. However, if the URL Group has configured a timeout, the setting for the URL Group takes precedence over the server session configuration.

Setting a timeout to zero on a server session causes the HTTP Server API to revert to the default value for that timer. For timers set on a URL Group, the server session timeout is used if present, otherwise the HTTP Server API default is used.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>