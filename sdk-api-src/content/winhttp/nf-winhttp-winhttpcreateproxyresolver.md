---
UID: NF:winhttp.WinHttpCreateProxyResolver
title: WinHttpCreateProxyResolver function (winhttp.h)
description: Creates a handle for use by WinHttpGetProxyForUrlEx.
helpviewer_keywords: ["WinHttpCreateProxyResolver","WinHttpCreateProxyResolver function [WinHTTP]","http.winhttpcreateproxyresolver","winhttp/WinHttpCreateProxyResolver"]
old-location: http\winhttpcreateproxyresolver.htm
tech.root: http
ms.assetid: 8d0058b5-964d-4bd8-b689-582875fc1d6e
ms.date: 12/05/2018
ms.keywords: WinHttpCreateProxyResolver, WinHttpCreateProxyResolver function [WinHTTP], http.winhttpcreateproxyresolver, winhttp/WinHttpCreateProxyResolver
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
 - WinHttpCreateProxyResolver
 - winhttp/WinHttpCreateProxyResolver
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
 - WinHttpCreateProxyResolver
---

# WinHttpCreateProxyResolver function


## -description

The <b>WinHttpCreateProxyResolver</b> function creates a handle for use by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.

## -parameters

### -param hSession [in]

Valid <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> WinHTTP session handle returned by a previous call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>. The session handle must be opened using <b>WINHTTP_FLAG_ASYNC</b>.

### -param phResolver [out]

A pointer to a new handle for use by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.  When finished or cancelling an outstanding operation, close this handle with <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hSession</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>hSession</i> is not the result of a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a> or <i>hSession</i> is not marked as asynchronous using <b>WINHTTP_FLAG_ASYNC</b>.

</td>
</tr>
</table>