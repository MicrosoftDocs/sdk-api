---
UID: NS:winhttp._WINHTTP_PROXY_RESULT
title: "_WINHTTP_PROXY_RESULT"
author: windows-sdk-content
description: The WINHTTP_PROXY_RESULT structure contains collection of proxy result entries provided by WinHttpGetProxyResult.
old-location: http\winhttp_proxy_result.htm
old-project: winhttp
ms.assetid: 6a621701-3325-4877-99ba-8580ad07739d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WINHTTP_PROXY_RESULT, WINHTTP_PROXY_RESULT structure [HTTP], _WINHTTP_PROXY_RESULT, http.winhttp_proxy_result, winhttp/WINHTTP_PROXY_RESULT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winhttp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WINHTTP_PROXY_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_PROXY_RESULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINHTTP_PROXY_RESULT structure


## -description


The <b>WINHTTP_PROXY_RESULT</b> structure contains  collection of proxy result entries provided by <a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>.


## -struct-fields




### -field cEntries

The number of entries in the <b>pEntries</b> array.


### -field pEntries

A pointer to an array of <a href="https://msdn.microsoft.com/d1652b34-67a9-40ad-a495-836147e5cc88">WINHTTP_PROXY_RESULT_ENTRY</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/d1652b34-67a9-40ad-a495-836147e5cc88">WINHTTP_PROXY_RESULT_ENTRY</a>



<a href="https://msdn.microsoft.com/0484bf54-066f-4a7f-8d1a-079eb4b001bd">WinHttpFreeProxyResult</a>



<a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>
 

 

