---
UID: NS:http._HTTP_TIMEOUT_LIMIT_INFO
title: HTTP_TIMEOUT_LIMIT_INFO
author: windows-sdk-content
description: Defines the application-specific connection timeout limits.
old-location: http\http_timeout_limit_info.htm
tech.root: http
ms.assetid: 900f4b4d-c34d-4994-b8eb-b3f15e54f29a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_TIMEOUT_LIMIT_INFO, *PHTTP_TIMEOUT_LIMIT_INFO structure [HTTP], HTTP_TIMEOUT_LIMIT_INFO, HTTP_TIMEOUT_LIMIT_INFO structure [HTTP], http.http_timeout_limit_info, http/*PHTTP_TIMEOUT_LIMIT_INFO, http/HTTP_TIMEOUT_LIMIT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_TIMEOUT_LIMIT_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_TIMEOUT_LIMIT_INFO, *PHTTP_TIMEOUT_LIMIT_INFO
req.redist: 
---

# HTTP_TIMEOUT_LIMIT_INFO structure


## -description


The <b>HTTP_TIMEOUT_LIMIT_INFO</b> structure defines the application-specific connection timeout limits.

This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServerTimeoutsProperty</a> on a URL Group, server session,  or request queue.


## -struct-fields




### -field Flags

The <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure that specifies whether the property is present.


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



This structure is used in the <a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>, and  <a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a> functions to set or query the connection timeouts. The following table lists the default timeouts.

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
 

Calling <a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a> or <a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a> to configure a connection timeout affects only the calling application and does not set driver wide timeout limits. The idle connection and header wait timers can be configured for all HTTP applications by calling <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>. Administrative privileges are required to configure HTTP Server API wide timeouts. HTTP Server API wide configurations affect all HTTP applications on the computer and persist when the computer is shut down.

The application-specific <b>IdleConnection</b>  and <b>HeaderWait</b> timers are set on a limited basis. The HTTP Server API cannot determine the request queue or URL group that the request is associated with until the headers have been parsed. Therefore, the HTTP Server API enforces the default <b>IdleConnection</b>  and <b>HeaderWait</b> timers for the first request on a connection.  Subsequent requests on a Keep-Alive connection will use the application specific timeouts.

Setting a timeout on a server session affects all the URL Groups under the server session. However, if the URL Group has configured a timeout, the setting for the URL Group takes precedence over the server session configuration.

Setting a timeout to zero on a server session causes the HTTP Server API to revert to the default value for that timer. For timers set on a URL Group, the server session timeout is used if present, otherwise the HTTP Server API default is used.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

