---
UID: NF:http.HttpReadFragmentFromCache
title: HttpReadFragmentFromCache function (http.h)
description: The HttpReadFragmentFromCache function retrieves a response fragment having a specified name from the HTTP Server API cache.
helpviewer_keywords: ["HttpReadFragmentFromCache","HttpReadFragmentFromCache function [HTTP]","_http_httpreadfragmentfromcache","http.httpreadfragmentfromcache","http/HttpReadFragmentFromCache"]
old-location: http\httpreadfragmentfromcache.htm
tech.root: http
ms.assetid: 2f066e1d-035f-4c1c-b854-de4a6ef58a58
ms.date: 12/05/2018
ms.keywords: HttpReadFragmentFromCache, HttpReadFragmentFromCache function [HTTP], _http_httpreadfragmentfromcache, http.httpreadfragmentfromcache, http/HttpReadFragmentFromCache
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
 - HttpReadFragmentFromCache
 - http/HttpReadFragmentFromCache
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
 - HttpReadFragmentFromCache
---

# HttpReadFragmentFromCache function


## -description

The 
<b>HttpReadFragmentFromCache</b> function retrieves a response fragment having a specified name from the HTTP Server API cache.

## -parameters

### -param RequestQueueHandle [in]

Handle to the request queue with which the specified response fragment is associated. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param UrlPrefix [in]

Pointer to a <a href="/windows/desktop/Http/urlprefix-strings">UrlPrefix string</a> that contains the name of the fragment to be retrieved. This must match a UrlPrefix string used in a previous successful call to <a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a>.

### -param ByteRange [in]

Optional pointer to an 
<a href="/windows/desktop/api/http/ns-http-http_byte_range">HTTP_BYTE_RANGE</a> structure that indicates a starting offset in the specified fragment and byte-count to be returned. <b>NULL</b> if not used, in which case the entire fragment is returned.

### -param Buffer [out]

Pointer to a buffer into which the function copies the requested fragment.

### -param BufferLength [in]

Size, in bytes, of the <i>pBuffer</i> buffer.

### -param BytesRead [out]

Optional pointer to a variable that receives the number of bytes to be written into the output buffer. If <i>BufferLength</i> is less than this number, the call fails with a return of ERROR_INSUFFICIENT_BUFFER, and the value pointed to by <i>pBytesRead</i> can be used to determine the minimum length of buffer required for the call to succeed. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesRead</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesRead</i> must contain a valid memory address, and not be set to <b>NULL</b>.

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
One or more of the supplied parameters is in an unusable form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pBuffer</i> is too small to receive all the requested data; the size of buffer required is pointed to by <i>pBytesRead</i> unless it was <b>NULL</b> or the call was asynchronous. In the case of an asynchronous call, the value pointed to by the <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverLappedResult</a> function is set to the buffer size required.

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



<a href="/windows/desktop/api/http/nf-http-httpflushresponsecache">HttpFlushResponseCache</a>