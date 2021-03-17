---
UID: NF:rpcndr.RpcSmClientFree
title: RpcSmClientFree function (rpcndr.h)
description: The RpcSmClientFree function frees memory returned from a client stub.
helpviewer_keywords: ["RpcSmClientFree","RpcSmClientFree function [RPC]","_rpc_rpcsmclientfree","rpc.rpcsmclientfree","rpcndr/RpcSmClientFree"]
old-location: rpc\rpcsmclientfree.htm
tech.root: Rpc
ms.assetid: b3e9a526-7b78-49a6-9550-e3f682cecfb8
ms.date: 12/05/2018
ms.keywords: RpcSmClientFree, RpcSmClientFree function [RPC], _rpc_rpcsmclientfree, rpc.rpcsmclientfree, rpcndr/RpcSmClientFree
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
 - RpcSmClientFree
 - rpcndr/RpcSmClientFree
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
 - RpcSmClientFree
---

# RpcSmClientFree function


## -description

The 
<b>RpcSmClientFree</b> function frees memory returned from a client stub.

## -parameters

### -param pNodeToFree

Pointer to memory returned from a client stub.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcSmClientFree</b> function releases memory allocated and returned from a client stub. The memory management handle of the thread calling this function must match the handle of the thread that made the RPC call. Use 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a> to pass handles from thread to thread.

Note that using 
<b>RpcSmClientFree</b> allows a function to free dynamically-allocated memory returned by an RPC call without knowing the memory-management environment from which it was called.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetclientallocfree">RpcSmSetClientAllocFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmswapclientallocfree">RpcSmSwapClientAllocFree</a>