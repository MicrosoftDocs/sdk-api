---
UID: NF:combaseapi.CoDecodeProxy
title: CoDecodeProxy function (combaseapi.h)
description: Locates the implementation of a Component Object Model (COM) interface in a server process given an interface to a proxied object.
helpviewer_keywords: ["CoDecodeProxy","CoDecodeProxy function [Windows Runtime]","combaseapi/CoDecodeProxy","winrt.codecodeproxy"]
old-location: winrt\codecodeproxy.htm
tech.root: WinRT
ms.assetid: C61C68B1-78CA-4052-9E24-629AB4083B86
ms.date: 12/05/2018
ms.keywords: CoDecodeProxy, CoDecodeProxy function [Windows Runtime], combaseapi/CoDecodeProxy, winrt.codecodeproxy
req.header: combaseapi.h
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
req.lib: Ole32.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoDecodeProxy
 - combaseapi/CoDecodeProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
api_name:
 - CoDecodeProxy
---

# CoDecodeProxy function


## -description

Locates the implementation of a Component Object Model (COM) interface in a server process given an  interface to a proxied object.

## -parameters

### -param dwClientPid [in]

The process ID of the process that contains the proxy.

### -param ui64ProxyAddress [in]

The address of an interface on a proxy to the object.  <i>ui64ProxyAddress</i> is considered a 64-bit value type, rather than a pointer  to a 64-bit value, and isn't a pointer to an object in the debugger process. Instead, this address is passed to the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> function.

### -param pServerInformation [out]

A structure that contains the process ID, the thread ID, and the address of the server.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The server information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is an app container, or the developer license is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_INVALID_IPID</b></dt>
</dl>
</td>
<td width="60%">
<i>ui64ProxyAddress</i> does not point to a proxy.

</td>
</tr>
</table>

## -remarks

The <b>CoDecodeProxy</b> function is a COM API that enables native debuggers to locate the implementation of a COM interface in a server process given an interface on a proxy to the object.


Also, the <b>CoDecodeProxy</b> function enables the debugger to monitor cross-apartment function calls and fail such calls when appropriate.

You can call the <b>CoDecodeProxy</b> function from a 32-bit or 64-bit process. <i>ui64ProxyAddress</i> can be a 32-bit or 64-bit address. The <b>CoDecodeProxy</b> function returns a 32-bit or 64-bit address in the <i>pServerInformation</i> field. If it returns a 64-bit address, you should pass the address to the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> function only from a 64-bit process.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>



<a href="/windows/desktop/api/combaseapi/ns-combaseapi-serverinformation">ServerInformation</a>