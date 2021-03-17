---
UID: NF:http.HttpWaitForDisconnectEx
title: HttpWaitForDisconnectEx function (http.h)
description: This function is an extension to HttpWaitForDisconnect.
helpviewer_keywords: ["HttpWaitForDisconnectEx","HttpWaitForDisconnectEx function [HTTP]","http.httpwaitfordisconnectex","http/HttpWaitForDisconnectEx"]
old-location: http\httpwaitfordisconnectex.htm
tech.root: http
ms.assetid: D4946ECF-0E0E-439E-AEE5-BF24BD73D2B6
ms.date: 12/05/2018
ms.keywords: HttpWaitForDisconnectEx, HttpWaitForDisconnectEx function [HTTP], http.httpwaitfordisconnectex, http/HttpWaitForDisconnectEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpWaitForDisconnectEx
 - http/HttpWaitForDisconnectEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpWaitForDisconnectEx
---

# HttpWaitForDisconnectEx function


## -description

This function is an extension to <a href="/windows/desktop/api/http/nf-http-httpwaitfordisconnect">HttpWaitForDisconnect</a>.<div class="alert"><b>Note</b>  Calling this API directly in your code is not recommended. Call <a href="/windows/desktop/api/http/nf-http-httpwaitfordisconnect">HttpWaitForDisconnect</a> instead.</div>
<div> </div>

## -parameters

### -param RequestQueueHandle [in]

### -param ConnectionId [in]

### -param Reserved

### -param Overlapped [in]

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>