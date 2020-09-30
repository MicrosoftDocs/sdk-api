---
UID: NF:http.HttpRemoveUrlFromUrlGroup
title: HttpRemoveUrlFromUrlGroup function (http.h)
description: Removes the specified URL from the group identified by the URL Group ID.
helpviewer_keywords: ["HTTP_URL_FLAG_REMOVE_ALL","HttpRemoveUrlFromUrlGroup","HttpRemoveUrlFromUrlGroup function [HTTP]","http.httpremoveurlfromurlgroup","http/HttpRemoveUrlFromUrlGroup"]
old-location: http\httpremoveurlfromurlgroup.htm
tech.root: http
ms.assetid: 9c5c1fec-f3b4-414f-a841-e360f5f4e4db
ms.date: 12/05/2018
ms.keywords: HTTP_URL_FLAG_REMOVE_ALL, HttpRemoveUrlFromUrlGroup, HttpRemoveUrlFromUrlGroup function [HTTP], http.httpremoveurlfromurlgroup, http/HttpRemoveUrlFromUrlGroup
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
 - HttpRemoveUrlFromUrlGroup
 - http/HttpRemoveUrlFromUrlGroup
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
 - HttpRemoveUrlFromUrlGroup
---

# HttpRemoveUrlFromUrlGroup function


## -description

The <b>HttpRemoveUrlFromUrlGroup</b> function removes the specified URL from  the group identified by the URL Group ID. This function removes one, or all, of the URLs from the group. 

This function replaces the HTTP version 1.0 <a href="/windows/desktop/api/http/nf-http-httpremoveurl">HttpRemoveUrl</a> function.

## -parameters

### -param UrlGroupId [in]

The ID of the URL group from which the URL specified in <i>pFullyQualifiedUrl</i> is removed.

### -param pFullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix String</a> that identifies the URL to be removed.

When <b>HTTP_URL_FLAG_REMOVE_ALL</b> is passed in the <i>Flags</i> parameter, all of the existing URL registrations for the URL Group identified in <i>UrlGroupId</i> are removed from the group. In this case, <i>pFullyQualifiedUrl</i> must be <b>NULL</b>.

### -param Flags [in]

The URL flags qualifying the URL that is removed. This  can be one of the following flags:

<table>
<tr>
<th>URL Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_URL_FLAG_REMOVE_ALL"></a><a id="http_url_flag_remove_all"></a><dl>
<dt><b>HTTP_URL_FLAG_REMOVE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Removes all of the URLs currently registered with the URL Group.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns NO_ERROR.

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
The URL Group does not exist.

The Flags parameter contains an invalid combination of flags.

The HTTP_URL_FLAG_REMOVE_ALL flag was set and the <i>pFullyQualifiedUrl</i> parameter was not set to <b>NULL</b>.

The application does not have permission to remove URLs from the Group. Only the application that created the URL Group can remove URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not have permission to deregister the URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified URL is not registered with the URL Group.

</td>
</tr>
</table>

## -remarks

The HTTP Server API supports existing applications using the version 1.0 URL registrations, however, new development with the HTTP Server API should use <b>HttpRemoveUrlFromUrlGroup</b>; do not use <a href="/windows/desktop/api/http/nf-http-httpremoveurl">HttpRemoveUrl</a>.

Applications should remove the URL added to the group by <a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>, when the URL is no longer required.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseurlgroup">HttpCloseUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurl">HttpRemoveUrl</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>