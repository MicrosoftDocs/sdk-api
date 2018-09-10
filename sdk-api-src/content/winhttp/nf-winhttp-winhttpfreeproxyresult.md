---
UID: NF:winhttp.WinHttpFreeProxyResult
title: WinHttpFreeProxyResult function
author: windows-sdk-content
description: The WinHttpFreeProxyResult function frees the data retrieved from a previous call to WinHttpGetProxyResult.
old-location: http\winhttpfreeproxyresult.htm
tech.root: WinHttp
ms.assetid: 0484bf54-066f-4a7f-8d1a-079eb4b001bd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WinHttpFreeProxyResult, WinHttpFreeProxyResult function [WinHTTP], http.winhttpfreeproxyresult, winhttp/WinHttpFreeProxyResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpFreeProxyResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinHttpFreeProxyResult function


## -description


The <b>WinHttpFreeProxyResult</b> function frees the data retrieved from a previous call to <a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>.


## -parameters




### -param pProxyResult [in, out]

A pointer to a <a href="https://msdn.microsoft.com/6a621701-3325-4877-99ba-8580ad07739d">WINHTTP_PROXY_RESULT</a> structure retrieved from a previous call to <a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>.  


## -returns



This function does not return a value.




## -remarks



Upon completion, all internal members of <i>pProxyResult</i> will be zeroed and the memory allocated to those members will be freed. If <i>pProxyResult</i> is an allocated pointer, the caller must free the pointer.



