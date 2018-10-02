---
UID: NF:http.HttpWaitForDisconnectEx
title: HttpWaitForDisconnectEx function
author: windows-sdk-content
description: This function is an extension to HttpWaitForDisconnect.
old-location: http\httpwaitfordisconnectex.htm
tech.root: Http
ms.assetid: D4946ECF-0E0E-439E-AEE5-BF24BD73D2B6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HttpWaitForDisconnectEx, HttpWaitForDisconnectEx function [HTTP], http.httpwaitfordisconnectex, http/HttpWaitForDisconnectEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HttpWaitForDisconnectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpWaitForDisconnectEx function


## -description


This function is an extension to <a href="https://msdn.microsoft.com/1f1c16c1-43ef-4e29-8d3d-8592ce6a6bf0">HttpWaitForDisconnect</a>.<div class="alert"><b>Note</b>  Calling this API directly in your code is not recommended. Call <a href="https://msdn.microsoft.com/1f1c16c1-43ef-4e29-8d3d-8592ce6a6bf0">HttpWaitForDisconnect</a> instead.</div>
<div> </div>



## -parameters




### -param RequestQueueHandle [in]


### -param ConnectionId [in]


### -param Reserved


### -param Overlapped

TBD




#### - pOverlapped [in]


## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>
 

 

