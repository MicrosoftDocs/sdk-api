---
UID: NF:http.HttpCancelHttpRequest
title: HttpCancelHttpRequest function (http.h)
description: The HttpCancelHttpRequest function cancels a specified reqest.
old-location: http\httpcancelhttprequest.htm
tech.root: http
ms.assetid: 9ece13ab-7b13-49b7-8d29-bbbb2755db52
ms.date: 12/05/2018
ms.keywords: HttpCancelHttpRequest, HttpCancelHttpRequest function [HTTP], http.httpcancelhttprequest, http/HttpCancelHttpRequest
f1_keywords:
- http/HttpCancelHttpRequest
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Http/processing-requests">Processing Requests</a>
 

 

