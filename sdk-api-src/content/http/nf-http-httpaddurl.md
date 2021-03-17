---
UID: NF:http.HttpAddUrl
title: HttpAddUrl function (http.h)
description: Registers a given URL so that requests that match it are routed to a specified HTTP Server API request queue.
helpviewer_keywords: ["HttpAddUrl","HttpAddUrl function [HTTP]","_http_httpaddurl","http.httpaddurl","http/HttpAddUrl"]
old-location: http\httpaddurl.htm
tech.root: http
ms.assetid: 76b228a0-6792-4184-bf0e-8638f3ab6b98
ms.date: 12/05/2018
ms.keywords: HttpAddUrl, HttpAddUrl function [HTTP], _http_httpaddurl, http.httpaddurl, http/HttpAddUrl
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
 - HttpAddUrl
 - http/HttpAddUrl
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
 - HttpAddUrl
---

# HttpAddUrl function


## -description

The 
<b>HttpAddUrl</b> function registers a given URL so that requests that match it are routed to a specified HTTP Server API request queue. An application can register multiple URLs to a single request queue using repeated calls to 
<b>HttpAddUrl</b>. For more information about how HTTP Server API matches request URLs to registered URLs, see 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix Strings</a>.

Starting with HTTP Server API Version 2.0,  applications should call <a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a> to register a URL; <b>HttpAddUrl</b> should not be used.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue to which requests for the specified URL are to be routed. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param FullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> that identifies the URL to be registered.

### -param Reserved

Reserved; must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have permission to register the URL.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified UrlPrefix conflicts with an existing registration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

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

As stated in the <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix Strings</a> topic, the scheme specification of the UrlPrefix to be registered must be either lower-case "http" or lower-case "https". No other substring is valid.

Also, it is not possible to register URLs having different schemes on the same port. That is, "http" and "https" schemes cannot coexist on a port.

Also be aware that 
<b>HttpAddUrl</b> registers any UrlPrefix passed to it as long as the string is well-formed. Any validation of existence, accessibility, ownership, or other characteristic of the specified URL namespace must be handled by the application.

To release the resources allocated as a result of the registration performed by 
<b>HttpAddUrl</b>, make a matching call to the 
<a href="/windows/desktop/api/http/nf-http-httpremoveurl">HttpRemoveUrl</a> function when your application has finished with the namespace involved.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurl">HttpRemoveUrl</a>