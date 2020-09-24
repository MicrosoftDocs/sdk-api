---
UID: NF:rpcndr.RpcSmSetClientAllocFree
title: RpcSmSetClientAllocFree function (rpcndr.h)
description: The RpcSmSetClientAllocFree function enables the memory allocation and release mechanisms used by the client stubs.
helpviewer_keywords: ["RpcSmSetClientAllocFree","RpcSmSetClientAllocFree function [RPC]","_rpc_rpcsmsetclientallocfree","rpc.rpcsmsetclientallocfree","rpcndr/RpcSmSetClientAllocFree"]
old-location: rpc\rpcsmsetclientallocfree.htm
tech.root: Rpc
ms.assetid: f6b6db72-c9af-44d1-9f84-26aaaa17691c
ms.date: 12/05/2018
ms.keywords: RpcSmSetClientAllocFree, RpcSmSetClientAllocFree function [RPC], _rpc_rpcsmsetclientallocfree, rpc.rpcsmsetclientallocfree, rpcndr/RpcSmSetClientAllocFree
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
 - RpcSmSetClientAllocFree
 - rpcndr/RpcSmSetClientAllocFree
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
 - RpcSmSetClientAllocFree
---

# RpcSmSetClientAllocFree function


## -description

The 
<b>RpcSmSetClientAllocFree</b> function enables the memory allocation and release mechanisms used by the client stubs.

## -parameters

### -param ClientAlloc

Function used to allocate memory.

### -param ClientFree

Function used to release memory and used with the function specified by <i>pfnAllocate</i>.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
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

By overriding the default routines used by the client stub to manage memory, 
<b>RpcSmSetClientAllocFree</b> establishes the memory allocation and memory-freeing mechanisms. Note that the default routines are <a href="/windows/desktop/Rpc/pointers-and-memory-allocation">free</a> and <b>malloc</b>, unless the remote call occurs within manager code. In this case, the default memory–management functions are 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>