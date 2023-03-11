---
UID: NF:http.HttpAddUrlToUrlGroup
title: HttpAddUrlToUrlGroup function (http.h)
description: Adds the specified URL to the URL Group identified by the URL Group ID.
helpviewer_keywords: ["HttpAddUrlToUrlGroup","HttpAddUrlToUrlGroup function [HTTP]","http.httpaddurltourlgroup","http/HttpAddUrlToUrlGroup"]
old-location: http\httpaddurltourlgroup.htm
tech.root: http
ms.assetid: e6bf68aa-d6a5-4079-b689-49cfc2303ba5
ms.date: 12/05/2018
ms.keywords: HttpAddUrlToUrlGroup, HttpAddUrlToUrlGroup function [HTTP], http.httpaddurltourlgroup, http/HttpAddUrlToUrlGroup
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
 - HttpAddUrlToUrlGroup
 - http/HttpAddUrlToUrlGroup
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
 - HttpAddUrlToUrlGroup
---

# HttpAddUrlToUrlGroup function


## -description

The <b>HttpAddUrlToUrlGroup</b> function adds the specified URL to  the URL Group identified by the URL Group ID.

 This function replaces the HTTP version 1.0 <a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a> function.

## -parameters

### -param UrlGroupId [in]

The group ID for the URL group to which requests for the specified URL are routed. The URL group is created by the <a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a> function.

### -param pFullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix String</a> that identifies the URL to be registered. If you are not running as an administrator, specify a port number greater than 1024, otherwise you may get an ERROR_ACCESS_DENIED error.

### -param UrlContext [in, optional]

The context that is associated with the URL registered in this call. The URL context is returned in the <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure with every request received on the URL specified in the <i>pFullyQualifiedUrl</i> parameter.

### -param Reserved [in]

Reserved. Must be zero.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>

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
The <i>UrlGroupId</i> does not exist.

 The <i>Reserved</i> parameter is not zero.

The application does not have permission to add URLs to the Group. Only the application that created the URL Group can add URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not have permission to register the URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified URL conflicts with an existing registration.

</td>
</tr>
</table>

## -remarks

The HTTP Server API supports existing applications using version 1.0 URL registrations, however, new development with the HTTP Server API should use <b>HttpAddUrlToUrlGroup</b>; <a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a> should not be used.

An application can add multiple URLs to a URL group using repeated calls to <b>HttpAddUrlToUrlGroup</b>. Requests that match the specified  URL are routed to the request queue associated with the URL group. For more information about how the HTTP Server API matches request URLs to registered URLs, see <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix Strings</a>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseurlgroup">HttpCloseUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>



<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix Strings</a>
