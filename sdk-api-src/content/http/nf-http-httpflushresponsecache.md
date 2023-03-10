---
UID: NF:http.HttpFlushResponseCache
title: HttpFlushResponseCache function (http.h)
description: Removes from the HTTP Server API cache associated with a given request queue all response fragments that have a name whose site portion matches a specified UrlPrefix.
helpviewer_keywords: ["HttpFlushResponseCache","HttpFlushResponseCache function [HTTP]","_http_httpflushresponsecache","http.httpflushresponsecache","http/HttpFlushResponseCache"]
old-location: http\httpflushresponsecache.htm
tech.root: http
ms.assetid: 5b7377cf-b4a9-45c7-8456-72a52c3778a0
ms.date: 12/05/2018
ms.keywords: HttpFlushResponseCache, HttpFlushResponseCache function [HTTP], _http_httpflushresponsecache, http.httpflushresponsecache, http/HttpFlushResponseCache
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
 - HttpFlushResponseCache
 - http/HttpFlushResponseCache
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
 - HttpFlushResponseCache
---

# HttpFlushResponseCache function


## -description

The 
<b>HttpFlushResponseCache</b> function removes from the HTTP Server API cache associated with a given request queue all response fragments that have a name whose site portion matches a specified UrlPrefix. The application must previously have called <a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a>, or <a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a> to add this UrlPrefix or a valid prefix of it to the request queue in question, and then called <a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a> to cache the associated response fragment or fragments.

## -parameters

### -param RequestQueueHandle [in]

Handle to the request queue with which this cache is associated. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param UrlPrefix [in]

Pointer to a 
<a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> to match against the site portion of fragment names. The application must previously have called <a href="/windows/desktop/api/http/nf-http-httpaddurl">HttpAddUrl</a> to add this UrlPrefix or a valid prefix of it to the request queue in question, and then called <a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a> to cache the associated response fragment.

### -param Flags [in]

This parameter can contain the following flag: 







#### HTTP_FLUSH_RESPONSE_FLAG_RECURSIVE

Causes response fragments that have names in which the site portion is a hierarchical descendant of the specified UrlPrefix to be removed from the fragment cache, in addition to those fragments having site portions that directly match.

### -param Overlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, or for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the cache operation is complete, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function is used asynchronously, a return value of ERROR_IO_PENDING indicates that the cache request is queued and  completes later through normal overlapped I/O completion mechanisms.

If the function fails, the return value is one of the following error codes.

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
One of the parameters are invalid.

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



<a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a>



<a href="/windows/desktop/api/http/nf-http-httpreadfragmentfromcache">HttpReadFragmentFromCache</a>