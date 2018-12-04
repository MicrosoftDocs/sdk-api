---
UID: NF:http.HttpReadFragmentFromCache
title: HttpReadFragmentFromCache function
author: windows-sdk-content
description: The HttpReadFragmentFromCache function retrieves a response fragment having a specified name from the HTTP Server API cache.
old-location: http\httpreadfragmentfromcache.htm
tech.root: http
ms.assetid: 2f066e1d-035f-4c1c-b854-de4a6ef58a58
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: HttpReadFragmentFromCache, HttpReadFragmentFromCache function [HTTP], _http_httpreadfragmentfromcache, http.httpreadfragmentfromcache, http/HttpReadFragmentFromCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpReadFragmentFromCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpReadFragmentFromCache function


## -description


The 
<b>HttpReadFragmentFromCache</b> function retrieves a response fragment having a specified name from the HTTP Server API cache.


## -parameters




### -param RequestQueueHandle [in]

Handle to the request queue with which the specified response fragment is associated. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param UrlPrefix [in]

Pointer to a <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> that contains the name of the fragment to be retrieved. This must match a UrlPrefix string used in a previous successful call to <a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>.


### -param ByteRange [in]

Optional pointer to an 
<a href="https://msdn.microsoft.com/a57d23cd-1e91-401a-b242-6549b1457594">HTTP_BYTE_RANGE</a> structure that indicates a starting offset in the specified fragment and byte-count to be returned. <b>NULL</b> if not used, in which case the entire fragment is returned.


### -param Buffer [out]

Pointer to a buffer into which the function copies the requested fragment.


### -param BufferLength [in]

Size, in bytes, of the <i>pBuffer</i> buffer.


### -param BytesRead [out]

Optional pointer to a variable that receives the number of bytes to be written into the output buffer. If <i>BufferLength</i> is less than this number, the call fails with a return of ERROR_INSUFFICIENT_BUFFER, and the value pointed to by <i>pBytesRead</i> can be used to determine the minimum length of buffer required for the call to succeed. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesRead</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesRead</i> must contain a valid memory address, and not be set to <b>NULL</b>.


### -param Overlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, or for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the cache operation is complete, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structures for synchronization, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.


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
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverLappedResult</a> function is set to the buffer size required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>



<a href="https://msdn.microsoft.com/5b7377cf-b4a9-45c7-8456-72a52c3778a0">HttpFlushResponseCache</a>
 

 

