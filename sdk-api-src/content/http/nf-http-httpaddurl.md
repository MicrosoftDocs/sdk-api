---
UID: NF:http.HttpAddUrl
title: HttpAddUrl function
author: windows-sdk-content
description: Registers a given URL so that requests that match it are routed to a specified HTTP Server API request queue.
old-location: http\httpaddurl.htm
old-project: http
ms.assetid: 76b228a0-6792-4184-bf0e-8638f3ab6b98
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpAddUrl, HttpAddUrl function [HTTP], _http_httpaddurl, http.httpaddurl, http/HttpAddUrl
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
 - HttpAddUrl
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpAddUrl function


## -description


The 
<b>HttpAddUrl</b> function registers a given URL so that requests that match it are routed to a specified HTTP Server API request queue. An application can register multiple URLs to a single request queue using repeated calls to 
<b>HttpAddUrl</b>. For more information about how HTTP Server API matches request URLs to registered URLs, see 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a>.

Starting with HTTP Server API Version 2.0,  applications should call <a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a> to register a URL; <b>HttpAddUrl</b> should not be used.


## -parameters




### -param RequestQueueHandle [in]

The handle to the request queue to which requests for the specified URL are to be routed. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param FullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> that identifies the URL to be registered.


### -param Reserved

Reserved; must be <b>NULL</b>.


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
The calling application does not have permission to register the URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DLL_INIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The calling application did not call 
<a href="https://msdn.microsoft.com/bc0648a9-bacf-4b09-aa4e-66aecbbdca3d">HttpInitialize</a> before calling this function.

</td>
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
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified UrlPrefix conflicts with an existing registration.

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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -remarks



As stated in the <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a> topic, the scheme specification of the UrlPrefix to be registered must be either lower-case "http" or lower-case "https". No other substring is valid.

Also, it is not possible to register URLs having different schemes on the same port. That is, "http" and "https" schemes cannot coexist on a port.

Also be aware that 
<b>HttpAddUrl</b> registers any UrlPrefix passed to it as long as the string is well-formed. Any validation of existence, accessibility, ownership, or other characteristic of the specified URL namespace must be handled by the application.

To release the resources allocated as a result of the registration performed by 
<b>HttpAddUrl</b>, make a matching call to the 
<a href="https://msdn.microsoft.com/21740d08-c280-44c1-8efb-1d21b4006039">HttpRemoveUrl</a> function when your application has finished with the namespace involved.




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>



<a href="https://msdn.microsoft.com/21740d08-c280-44c1-8efb-1d21b4006039">HttpRemoveUrl</a>
 

 

