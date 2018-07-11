---
UID: NF:http.HttpCancelHttpRequest
title: HttpCancelHttpRequest function
author: windows-sdk-content
description: The HttpCancelHttpRequest function cancels a specified reqest.
old-location: http\httpcancelhttprequest.htm
old-project: http
ms.assetid: 9ece13ab-7b13-49b7-8d29-bbbb2755db52
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: HttpCancelHttpRequest, HttpCancelHttpRequest function [HTTP], http.httpcancelhttprequest, http/HttpCancelHttpRequest
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
 - HttpCancelHttpRequest
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpCancelHttpRequest function


## -description


The <b>HttpCancelHttpRequest</b> function cancels a specified reqest.


## -parameters




### -param RequestQueueHandle

TBD


### -param RequestId [in]

The ID of the request to be canceled.


### -param OPTIONAL

TBD




#### - ReqQueueHandle [in]

A handle to the request queue from which the request came.


#### - pOverlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/fb170d73-c26d-4bec-abed-b614b7dad322">Processing Requests</a>
 

 

