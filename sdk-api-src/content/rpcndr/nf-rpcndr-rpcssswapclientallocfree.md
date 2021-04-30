---
UID: NF:rpcndr.RpcSsSwapClientAllocFree
title: RpcSsSwapClientAllocFree function (rpcndr.h)
description: The RpcSsSwapClientAllocFree function exchanges the memory allocation and release mechanisms used by the client stubs with those supplied by the client.
helpviewer_keywords: ["RpcSsSwapClientAllocFree","RpcSsSwapClientAllocFree function [RPC]","_rpc_rpcssswapclientallocfree","rpc.rpcssswapclientallocfree","rpcndr/RpcSsSwapClientAllocFree"]
old-location: rpc\rpcssswapclientallocfree.htm
tech.root: Rpc
ms.assetid: 1ed7161b-f49c-48bc-8b64-3a9596833f19
ms.date: 12/05/2018
ms.keywords: RpcSsSwapClientAllocFree, RpcSsSwapClientAllocFree function [RPC], _rpc_rpcssswapclientallocfree, rpc.rpcssswapclientallocfree, rpcndr/RpcSsSwapClientAllocFree
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
 - RpcSsSwapClientAllocFree
 - rpcndr/RpcSsSwapClientAllocFree
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
 - RpcSsSwapClientAllocFree
---

# RpcSsSwapClientAllocFree function


## -description

The 
<b>RpcSsSwapClientAllocFree</b> function exchanges the memory allocation and release mechanisms used by the client stubs with those supplied by the client.

## -parameters

### -param ClientAlloc

New function to allocate memory.

### -param ClientFree

New function to release memory.

### -param OldClientAlloc

Returns the previous memory-allocation function.

### -param OldClientFree

Returns the previous memory-freeing function.

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

<b>RpcSsSwapClientAllocFree</b> exchanges the current memory allocation and memory freeing mechanisms with those supplied by the client.

<div class="alert"><b>Note</b>  <b>RpcSsSwapClientAllocFree</b> raises exceptions, unlike 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmswapclientallocfree">RpcSmSwapClientAllocFree</a>, which returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmswapclientallocfree">RpcSmSwapClientAllocFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetclientallocfree">RpcSsSetClientAllocFree</a>