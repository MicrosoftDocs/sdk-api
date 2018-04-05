---
UID: NF:winhttp.WinHttpGetProxyResult
title: WinHttpGetProxyResult function
author: windows-driver-content
description: The WinHttpGetProxyResult function retrieves the results of a call to WinHttpGetProxyForUrlEx.
old-location: http\winhttpgetproxyresult.htm
old-project: WinHttp
ms.assetid: f594e588-b3da-4afb-a5f9-552759bca148
ms.author: windowsdriverdev
ms.date: 3/8/2018
ms.keywords: WinHttpGetProxyResult, WinHttpGetProxyResult function [WinHTTP], http.winhttpgetproxyresult, winhttp/WinHttpGetProxyResult
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
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winhttp.dll
api_name:
-	WinHttpGetProxyResult
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpGetProxyResult function


## -description


The <b>WinHttpGetProxyResult</b> function retrieves the results of a call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


## -parameters




### -param hResolver [in]

The resolver handle used to issue a previously completed call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


### -param pProxyResult [out]

A pointer to a <a href="https://msdn.microsoft.com/6a621701-3325-4877-99ba-8580ad07739d">WINHTTP_PROXY_RESULT</a> structure that contains the results of a previous call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.  The results must be freed by calling <a href="https://msdn.microsoft.com/0484bf54-066f-4a7f-8d1a-079eb4b001bd">WinHttpFreeProxyResult</a>.


## -returns



A status code indicating the result of the operation.

<table>
<tr>
<th>The following codes may be returned.</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The resolver handle has not successfully completed a call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.

</td>
</tr>
</table>
 



