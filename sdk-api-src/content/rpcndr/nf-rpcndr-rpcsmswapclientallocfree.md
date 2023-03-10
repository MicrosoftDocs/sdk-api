---
UID: NF:rpcndr.RpcSmSwapClientAllocFree
title: RpcSmSwapClientAllocFree function (rpcndr.h)
description: The RpcSmSwapClientAllocFree function exchanges the client stub's memory-allocation and memory-freeing mechanisms with those supplied by the client.
helpviewer_keywords: ["RpcSmSwapClientAllocFree","RpcSmSwapClientAllocFree function [RPC]","_rpc_rpcsmswapclientallocfree","rpc.rpcsmswapclientallocfree","rpcndr/RpcSmSwapClientAllocFree"]
old-location: rpc\rpcsmswapclientallocfree.htm
tech.root: Rpc
ms.assetid: f07df5ec-0798-4cd2-a2f5-73e6245a7020
ms.date: 12/05/2018
ms.keywords: RpcSmSwapClientAllocFree, RpcSmSwapClientAllocFree function [RPC], _rpc_rpcsmswapclientallocfree, rpc.rpcsmswapclientallocfree, rpcndr/RpcSmSwapClientAllocFree
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
 - RpcSmSwapClientAllocFree
 - rpcndr/RpcSmSwapClientAllocFree
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
 - RpcSmSwapClientAllocFree
---

# RpcSmSwapClientAllocFree function


## -description

The 
<b>RpcSmSwapClientAllocFree</b> function exchanges the client stub's memory-allocation and memory-freeing mechanisms with those supplied by the client.

## -parameters

### -param ClientAlloc

New memory-allocation function.

### -param ClientFree

New memory-releasing function.

### -param OldClientAlloc

Returns the previous memory-allocation function before the call to this function.

### -param OldClientFree

Returns the previous memory-releasing function before the call to this function.

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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetclientallocfree">RpcSmSetClientAllocFree</a>