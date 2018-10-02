---
UID: NF:http.HttpAddFragmentToCache
title: HttpAddFragmentToCache function
author: windows-sdk-content
description: The HttpAddFragmentToCache function caches a data fragment with a specified name by which it can be retrieved, or updates data cached under a specified name.
old-location: http\httpaddfragmenttocache.htm
tech.root: Http
ms.assetid: caef2e93-39cd-4282-97d9-870f8236d8c4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HttpAddFragmentToCache, HttpAddFragmentToCache function [HTTP], _http_httpaddfragmenttocache, http.httpaddfragmenttocache, http/HttpAddFragmentToCache
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
 - HttpAddFragmentToCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpAddFragmentToCache function


## -description


The 
<b>HttpAddFragmentToCache</b> function caches a data fragment with a specified name by which it can be retrieved, or updates data cached under a specified name. Such cached data fragments can be used repeatedly to construct dynamic responses without the expense of disk reads. For example, a response composed of text and three images could be assembled dynamically from four or more cached fragments at the time a request is processed.


## -parameters




### -param RequestQueueHandle [in]

Handle to the request queue with which this cache is associated. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param UrlPrefix [in]

Pointer to a  <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> that the application uses in subsequent calls to 
<a href="https://msdn.microsoft.com/0183584f-105e-4fa3-8991-d3f2dfca1d62">HttpSendHttpResponse</a> to identify this cache entry. The application must have called <b>HttpAddUrl</b> previously with the same handle as in the <i>ReqQueueHandle</i> parameter, and with  either  this identical UrlPrefix string or a valid prefix of it.

Like any UrlPrefix, this string must take the form "scheme://host:port/relativeURI"; for example, http://www.mysite.com:80/image1.gif.


### -param DataChunk [in]

Pointer to an 
<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a> structure that specifies an entity body data block to cache under the name pointed to by <i>pUrlPrefix</i>.


### -param CachePolicy [in]

Pointer to an 
<a href="https://msdn.microsoft.com/91fcbf35-ef8b-4f70-9c31-3f741c0e2f6e">HTTP_CACHE_POLICY</a> structure that specifies how this data fragment should be cached.


### -param Overlapped

TBD




#### - pOverlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, or for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks the calling thread until the cache operation is complete, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structures for synchronization, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.


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
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/5b7377cf-b4a9-45c7-8456-72a52c3778a0">HttpFlushResponseCache</a>



<a href="https://msdn.microsoft.com/2f066e1d-035f-4c1c-b854-de4a6ef58a58">HttpReadFragmentFromCache</a>
 

 

