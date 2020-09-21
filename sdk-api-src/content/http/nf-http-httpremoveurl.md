---
UID: NF:http.HttpRemoveUrl
title: HttpRemoveUrl function (http.h)
description: Causes the system to stop routing requests that match a specified UrlPrefix string to a specified request queue.
helpviewer_keywords: ["HttpRemoveUrl","HttpRemoveUrl function [HTTP]","_http_httpremoveurl","http.httpremoveurl","http/HttpRemoveUrl"]
old-location: http\httpremoveurl.htm
tech.root: http
ms.assetid: 21740d08-c280-44c1-8efb-1d21b4006039
ms.date: 12/05/2018
ms.keywords: HttpRemoveUrl, HttpRemoveUrl function [HTTP], _http_httpremoveurl, http.httpremoveurl, http/HttpRemoveUrl
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
 - HttpRemoveUrl
 - http/HttpRemoveUrl
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
 - HttpRemoveUrl
---

# HttpRemoveUrl function


## -description

The 
<b>HttpRemoveUrl</b> function causes the system to stop routing requests that match a specified 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> to a specified request queue.

Starting with HTTP Server API Version 2.0,  applications should call <a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a> to register a URL; <b>HttpRemoveUrl</b> should not be used.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue from which the URL registration is to be removed. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param FullyQualifiedUrl [in]

A pointer to a 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a>  registered to the specified request queue. This string must be identical to the one passed to 
<a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a> to register the UrlPrefix; even a nomenclature change in an IPv6 address is not accepted.

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
The calling application does not have permission to remove the URL.

</td>
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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified UrlPrefix could not be found in the registration database.

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

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a>