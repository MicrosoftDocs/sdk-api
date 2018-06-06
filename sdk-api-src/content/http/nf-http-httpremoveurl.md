---
UID: NF:http.HttpRemoveUrl
title: HttpRemoveUrl function
author: windows-sdk-content
description: Causes the system to stop routing requests that match a specified UrlPrefix string to a specified request queue.
old-location: http\httpremoveurl.htm
old-project: Http
ms.assetid: 21740d08-c280-44c1-8efb-1d21b4006039
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HttpRemoveUrl, HttpRemoveUrl function [HTTP], _http_httpremoveurl, http.httpremoveurl, http/HttpRemoveUrl
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpRemoveUrl
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpRemoveUrl function


## -description


The 
<b>HttpRemoveUrl</b> function causes the system to stop routing requests that match a specified 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> to a specified request queue.

Starting with HTTP Server API Version 2.0,  applications should call <a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a> to register a URL; <b>HttpRemoveUrl</b> should not be used.


## -parameters




### -param RequestQueueHandle

TBD


### -param FullyQualifiedUrl

TBD




#### - ReqQueueHandle [in]

The handle to the request queue from which the URL registration is to be removed. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


#### - pFullyQualifiedUrl [in]

A pointer to a 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a>  registered to the specified request queue. This string must be identical to the one passed to 
<a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a> to register the UrlPrefix; even a nomenclature change in an IPv6 address is not accepted.


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
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a>



<a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a>
 

 

