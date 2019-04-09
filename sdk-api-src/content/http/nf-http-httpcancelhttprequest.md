---
UID: NF:http.HttpCancelHttpRequest
title: HttpCancelHttpRequest function (http.h)
author: windows-sdk-content
description: The HttpCancelHttpRequest function cancels a specified reqest.
old-location: http\httpcancelhttprequest.htm
tech.root: http
ms.assetid: 9ece13ab-7b13-49b7-8d29-bbbb2755db52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HttpCancelHttpRequest, HttpCancelHttpRequest function [HTTP], http.httpcancelhttprequest, http/HttpCancelHttpRequest
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
 - HttpCancelHttpRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpCancelHttpRequest function


## -description


The <b>HttpCancelHttpRequest</b> function cancels a specified reqest.


## -parameters




### -param RequestQueueHandle [in]

A handle to the request queue from which the request came.


### -param RequestId [in]

The ID of the request to be canceled.


### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/fb170d73-c26d-4bec-abed-b614b7dad322">Processing Requests</a>
 

 

