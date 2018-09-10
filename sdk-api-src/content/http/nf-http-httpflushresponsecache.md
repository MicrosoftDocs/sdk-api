---
UID: NF:http.HttpFlushResponseCache
title: HttpFlushResponseCache function
author: windows-sdk-content
description: Removes from the HTTP Server API cache associated with a given request queue all response fragments that have a name whose site portion matches a specified UrlPrefix.
old-location: http\httpflushresponsecache.htm
tech.root: http
ms.assetid: 5b7377cf-b4a9-45c7-8456-72a52c3778a0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpFlushResponseCache, HttpFlushResponseCache function [HTTP], _http_httpflushresponsecache, http.httpflushresponsecache, http/HttpFlushResponseCache
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
 - HttpFlushResponseCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpFlushResponseCache function


## -description


The 
<b>HttpFlushResponseCache</b> function removes from the HTTP Server API cache associated with a given request queue all response fragments that have a name whose site portion matches a specified UrlPrefix. The application must previously have called <a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a>, or <a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a> to add this UrlPrefix or a valid prefix of it to the request queue in question, and then called <a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a> to cache the associated response fragment or fragments.


## -parameters




### -param RequestQueueHandle [in]

Handle to the request queue with which this cache is associated. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param UrlPrefix [in]

Pointer to a 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> to match against the site portion of fragment names. The application must previously have called <a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a> to add this UrlPrefix or a valid prefix of it to the request queue in question, and then called <a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a> to cache the associated response fragment.


### -param Flags [in]

This parameter can contain the following flag: 







#### HTTP_FLUSH_RESPONSE_FLAG_RECURSIVE

Causes response fragments that have names in which the site portion is a hierarchical descendant of the specified UrlPrefix to be removed from the fragment cache, in addition to those fragments having site portions that directly match.


### -param Overlapped

TBD




#### - pOverlapped [in]

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
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>



<a href="https://msdn.microsoft.com/2f066e1d-035f-4c1c-b854-de4a6ef58a58">HttpReadFragmentFromCache</a>
 

 

