---
UID: NF:http.HttpSetRequestQueueProperty
title: HttpSetRequestQueueProperty function (http.h)
description: Sets a new property or modifies an existing property on the request queue identified by the specified handle.
helpviewer_keywords: ["HttpServer503VerbosityProperty","HttpServerQueueLengthProperty","HttpServerStateProperty","HttpSetRequestQueueProperty","HttpSetRequestQueueProperty function [HTTP]","http.httpsetrequestqueueproperty","http/HttpSetRequestQueueProperty"]
old-location: http\httpsetrequestqueueproperty.htm
tech.root: http
ms.assetid: 56111cc0-94c8-47dc-a3bb-ffc5dae772fe
ms.date: 12/05/2018
ms.keywords: HttpServer503VerbosityProperty, HttpServerQueueLengthProperty, HttpServerStateProperty, HttpSetRequestQueueProperty, HttpSetRequestQueueProperty function [HTTP], http.httpsetrequestqueueproperty, http/HttpSetRequestQueueProperty
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
 - HttpSetRequestQueueProperty
 - http/HttpSetRequestQueueProperty
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
 - HttpSetRequestQueueProperty
---

# HttpSetRequestQueueProperty function


## -description

The <b>HttpSetRequestQueueProperty</b> function sets a new property or modifies an existing property on the request queue identified by the specified handle.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue on which the property is set. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

### -param Property [in]

A member of the  <a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a> enumeration describing the property type that is set. This must be one of the following:

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServer503VerbosityProperty"></a><a id="httpserver503verbosityproperty"></a><a id="HTTPSERVER503VERBOSITYPROPERTY"></a><dl>
<dt><b>HttpServer503VerbosityProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the current verbosity level of 503 responses generated for the request queue.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQueueLengthProperty"></a><a id="httpserverqueuelengthproperty"></a><a id="HTTPSERVERQUEUELENGTHPROPERTY"></a><dl>
<dt><b>HttpServerQueueLengthProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the limit on the number of outstanding requests in the request queue.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerStateProperty"></a><a id="httpserverstateproperty"></a><a id="HTTPSERVERSTATEPROPERTY"></a><dl>
<dt><b>HttpServerStateProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the  state of the request queue. The state must be either active or inactive.


</td>
</tr>
</table>

### -param PropertyInformation [in]

A pointer to the buffer that contains the property information.

<i>pPropertyInformation</i> points to one of the following property information types based on the property that is set.<table>
<tr>
<th>Property</th>
<th> Configuration Type</th>
</tr>
<tr>
<td>HttpServerStateProperty</td>
<td>
<a href="/windows/desktop/api/http/ne-http-http_enabled_state">HTTP_ENABLED_STATE</a> enumeration</td>
</tr>
<tr>
<td>HttpServerQueueLengthProperty</td>
<td>ULONG</td>
</tr>
<tr>
<td>HttpServer503VerbosityProperty</td>
<td>
<a href="/windows/desktop/api/http/ne-http-http_503_response_verbosity">HTTP_503_RESPONSE_VERBOSITY</a> enumeration</td>
</tr>
</table>

### -param PropertyInformationLength [in]

The length, in bytes, of the buffer pointed to by the <i>pPropertyInformation</i> parameter.

### -param Reserved1 [in]

Reserved. Must be zero.

### -param Reserved2 [in]

Reserved. Must be <b>NULL</b>.

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
The <i>Reserved</i> parameter is not zero or the  <i>pReserved</i> parameter is not <b>NULL</b>.

The property type specified in the <i>Property</i> parameter is not supported for request queues.

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The application does not have permission to set properties on the request queue. Only the application that created the request queue can set the properties.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The handle to the request queue is an HTTP version 1.0 handle. Property management is only supported on HTTP version 2.0 or later request queues.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpshutdownrequestqueue">HttpShutdownRequestQueue</a>