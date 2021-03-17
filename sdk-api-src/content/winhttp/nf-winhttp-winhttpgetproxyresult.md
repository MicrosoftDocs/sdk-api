---
UID: NF:winhttp.WinHttpGetProxyResult
title: WinHttpGetProxyResult function (winhttp.h)
description: The WinHttpGetProxyResult function retrieves the results of a call to WinHttpGetProxyForUrlEx.
helpviewer_keywords: ["WinHttpGetProxyResult","WinHttpGetProxyResult function [WinHTTP]","http.winhttpgetproxyresult","winhttp/WinHttpGetProxyResult"]
old-location: http\winhttpgetproxyresult.htm
tech.root: http
ms.assetid: f594e588-b3da-4afb-a5f9-552759bca148
ms.date: 12/05/2018
ms.keywords: WinHttpGetProxyResult, WinHttpGetProxyResult function [WinHTTP], http.winhttpgetproxyresult, winhttp/WinHttpGetProxyResult
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpGetProxyResult
 - winhttp/WinHttpGetProxyResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpGetProxyResult
---

# WinHttpGetProxyResult function


## -description

The <b>WinHttpGetProxyResult</b> function retrieves the results of a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.

## -parameters

### -param hResolver [in]

The resolver handle used to issue a previously completed call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.

### -param pProxyResult [out]

A pointer to a <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result">WINHTTP_PROXY_RESULT</a> structure that contains the results of a previous call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.  The results must be freed by calling <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpfreeproxyresult">WinHttpFreeProxyResult</a>.

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
The resolver handle has not successfully completed a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.

</td>
</tr>
</table>