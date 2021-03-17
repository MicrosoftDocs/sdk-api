---
UID: NF:rpcndr.RpcSsAllocate
title: RpcSsAllocate function (rpcndr.h)
description: The RpcSsAllocate function allocates memory within the RPC stub memory-management function, and returns a pointer to the allocated memory or NULL.
helpviewer_keywords: ["RpcSsAllocate","RpcSsAllocate function [RPC]","_rpc_rpcssallocate","rpc.rpcssallocate","rpcndr/RpcSsAllocate"]
old-location: rpc\rpcssallocate.htm
tech.root: Rpc
ms.assetid: d1c1af46-63c5-4e50-abfb-c4f251972427
ms.date: 12/05/2018
ms.keywords: RpcSsAllocate, RpcSsAllocate function [RPC], _rpc_rpcssallocate, rpc.rpcssallocate, rpcndr/RpcSsAllocate
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcSsAllocate
 - rpcndr/RpcSsAllocate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSsAllocate
---

# RpcSsAllocate function


## -description

The 
<b>RpcSsAllocate</b> function allocates memory within the RPC stub memory-management function, and returns a pointer to the allocated memory or <b>NULL</b>.

## -parameters

### -param Size

Size of memory to allocate, in bytes.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcSsAllocate</b> function allows an application to allocate memory within the RPC stub memory–management function. Prior to calling 
<b>RpcSsAllocate</b>, the memory-management environment must already be established. For memory management called within the stub, the stub itself usually establishes the necessary environment. For more information, see 
<a href="/windows/desktop/Rpc/memory-management">Memory Management</a>. When using 
<b>RpcSsAllocate</b> to allocate memory not called from the stub, the application must call 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssenableallocate">RpcSsEnableAllocate</a> to establish the required memory-management environment.

The 
<b>RpcSsAllocate</b> routine returns a pointer to the allocated memory, if the call was successful. Otherwise, it raises an exception.

When the stub establishes the memory management, it frees any memory allocated by 
<b>RpcSsAllocate</b>. The application can free such memory before returning to the calling stub by calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>.

By contrast, when the application establishes the memory management, it must free any allocated memory. It does so by calling either 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a> or 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdisableallocate">RpcSsDisableAllocate</a>.

To manage the same memory within the stub memory–management environment, multiple threads can call 
<b>RpcSsAllocate</b> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>. In this case, the threads must share the same stub memory management–thread handle. Applications pass thread handles from thread-to-thread by calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RPCSsSetThreadHandle</a>.

<div class="alert"><b>Note</b>  The 
<b>RpcSsAllocate</b> routine raises exceptions, unlike 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>, which returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdisableallocate">RpcSsDisableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssenableallocate">RpcSsEnableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a>