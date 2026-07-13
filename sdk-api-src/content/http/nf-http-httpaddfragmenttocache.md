---
UID: NF:http.HttpAddFragmentToCache
title: HttpAddFragmentToCache function (http.h)
description: The HttpAddFragmentToCache function caches a data fragment with a specified name by which it can be retrieved, or updates data cached under a specified name.
helpviewer_keywords: ["HttpAddFragmentToCache","HttpAddFragmentToCache function [HTTP]","_http_httpaddfragmenttocache","http.httpaddfragmenttocache","http/HttpAddFragmentToCache"]
old-location: http\httpaddfragmenttocache.htm
tech.root: http
ms.assetid: caef2e93-39cd-4282-97d9-870f8236d8c4
ms.date: 12/05/2018
ms.keywords: HttpAddFragmentToCache, HttpAddFragmentToCache function [HTTP], _http_httpaddfragmenttocache, http.httpaddfragmenttocache, http/HttpAddFragmentToCache
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
 - HttpAddFragmentToCache
 - http/HttpAddFragmentToCache
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
 - HttpAddFragmentToCache
---

# HttpAddFragmentToCache function


## -description

The 
<b>HttpAddFragmentToCache</b> function caches a data fragment with a specified name by which it can be retrieved, or updates data cached under a specified name. Such cached data fragments can be used repeatedly to construct dynamic responses without the expense of disk reads. For example, a response composed of text and three images could be assembled dynamically from four or more cached fragments at the time a request is processed.

## -parameters

### -param RequestQueueHandle [in]

Handle to the request queue with which this cache is associated. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param UrlPrefix [in]

Pointer to a  <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> that the application uses in subsequent calls to 
<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> to identify this cache entry. The application must have called <b>HttpAddUrl</b> previously with the same handle as in the <i>ReqQueueHandle</i> parameter, and with  either  this identical UrlPrefix string or a valid prefix of it.

Like any UrlPrefix, this string must take the form "scheme://host:port/relativeURI"; for example, `http://www.mysite.com:80/image1.gif`.

### -param DataChunk [in]

Pointer to an 
<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a> structure that specifies an entity body data block to cache under the name pointed to by <i>pUrlPrefix</i>.

### -param CachePolicy [in]

Pointer to an 
<a href="/windows/desktop/api/http/ns-http-http_cache_policy">HTTP_CACHE_POLICY</a> structure that specifies how this data fragment should be cached.

### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, or for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks the calling thread until the cache operation is complete, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function is used asynchronously, a return value of ERROR_IO_PENDING indicates that the cache request is queued and will complete later through normal overlapped I/O completion mechanisms.

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
One or more of the supplied parameters is in an unusable form.

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



<a href="/windows/desktop/api/http/nf-http-httpflushresponsecache">HttpFlushResponseCache</a>



<a href="/windows/desktop/api/http/nf-http-httpreadfragmentfromcache">HttpReadFragmentFromCache</a>