---
UID: NF:http.HttpCloseRequestQueue
title: HttpCloseRequestQueue function
author: windows-sdk-content
description: Closes the handle to the specified request queue created by HttpCreateRequestQueue.
old-location: http\httpcloserequestqueue.htm
old-project: Http
ms.assetid: dfbc2d32-c1f6-41b1-8f4f-9e5e9f6dd9e1
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HttpCloseRequestQueue, HttpCloseRequestQueue function [HTTP], http.httpcloserequestqueue, http/HttpCloseRequestQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - HttpCloseRequestQueue
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpCloseRequestQueue function


## -description


The <b>HttpCloseRequestQueue</b> function closes the handle to the specified request queue created by <a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>.

The application must close the request queue when it is no longer required.


## -parameters




### -param RequestQueueHandle

TBD




#### - ReqQueueHandle [in]

The handle to the request queue that is closed. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.

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
The application does not have permission to close the request queue. Only the application that created the request queue can close it.

</td>
</tr>
</table>
 




## -remarks



Applications  should not call <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> on the request queue handle; instead, they should call <b>HttpCloseRequestQueue</b> to ensure that all the resources are released.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>



<a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/f6640565-a5a1-4a71-938c-1adf54beb40a">HttpShutdownRequestQueue</a>
 

 

