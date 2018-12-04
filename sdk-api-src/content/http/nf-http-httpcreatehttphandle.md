---
UID: NF:http.HttpCreateHttpHandle
title: HttpCreateHttpHandle function
author: windows-sdk-content
description: Creates an HTTP request queue for the calling application and returns a handle to it.
old-location: http\httpcreatehttphandle.htm
tech.root: http
ms.assetid: c3741092-c23a-465f-9a65-5bcbf977fad3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: HttpCreateHttpHandle, HttpCreateHttpHandle function [HTTP], _http_httpcreatehttphandle, http.httpcreatehttphandle, http/HttpCreateHttpHandle
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
 - HttpCreateHttpHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpCreateHttpHandle function


## -description


The 
<b>HttpCreateHttpHandle</b> function creates an HTTP request queue for the calling application and returns a handle to it.

Starting with HTTP Server API Version 2.0,  applications should call <a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> to create the request queue; <b>HttpCreateHttpHandle</b> should not be used.


## -parameters




### -param RequestQueueHandle [out]

A pointer to a variable that receives a handle to the request queue.


### -param Reserved [in]

Reserved. This parameter must be zero.


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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -remarks



The request queue enables the calling application to receive requests for particular URLs. The calling application uses the 
<a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a> function to specify the URL for which it should receive requests.

An application should use a single request queue to receive requests. Using multiple request queues from a single process does not increase response time or throughput.

When an application has finished receiving requests, it should call the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle.




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a>



<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>
 

 

