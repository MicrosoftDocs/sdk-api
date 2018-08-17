---
UID: NF:winhttp.WinHttpCreateProxyResolver
title: WinHttpCreateProxyResolver function
author: windows-sdk-content
description: Creates a handle for use by WinHttpGetProxyForUrlEx.
old-location: http\winhttpcreateproxyresolver.htm
old-project: winhttp
ms.assetid: 8d0058b5-964d-4bd8-b689-582875fc1d6e
ms.author: windowssdkdev
ms.date: 08/09/2018
ms.keywords: WinHttpCreateProxyResolver, WinHttpCreateProxyResolver function [WinHTTP], http.winhttpcreateproxyresolver, winhttp/WinHttpCreateProxyResolver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCreateProxyResolver
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpCreateProxyResolver function


## -description


The <b>WinHttpCreateProxyResolver</b> function creates a handle for use by <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


## -parameters




### -param hSession [in]

Valid <a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> WinHTTP session handle returned by a previous call to 
<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>. The session handle must be opened using <b>WINHTTP_FLAG_ASYNC</b>.


### -param phResolver [out]

A pointer to a new handle for use by <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.  When finished or cancelling an outstanding operation, close this handle with <a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>.


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
<i>hSession</i> is not the result of a call to <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a> or <i>hSession</i> is not marked as asynchronous using <b>WINHTTP_FLAG_ASYNC</b>.

</td>
</tr>
</table>
 



