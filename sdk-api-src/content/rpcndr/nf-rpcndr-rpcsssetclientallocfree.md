---
UID: NF:rpcndr.RpcSsSetClientAllocFree
title: RpcSsSetClientAllocFree function (rpcndr.h)
description: The RpcSsSetClientAllocFree function enables the memory allocation and release mechanisms used by the client stubs.
helpviewer_keywords: ["RpcSsSetClientAllocFree","RpcSsSetClientAllocFree function [RPC]","_rpc_rpcsssetclientallocfree","rpc.rpcsssetclientallocfree","rpcndr/RpcSsSetClientAllocFree"]
old-location: rpc\rpcsssetclientallocfree.htm
tech.root: Rpc
ms.assetid: a63dab9e-0644-4a24-9762-8cc8a4f6ea05
ms.date: 12/05/2018
ms.keywords: RpcSsSetClientAllocFree, RpcSsSetClientAllocFree function [RPC], _rpc_rpcsssetclientallocfree, rpc.rpcsssetclientallocfree, rpcndr/RpcSsSetClientAllocFree
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
 - RpcSsSetClientAllocFree
 - rpcndr/RpcSsSetClientAllocFree
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
 - RpcSsSetClientAllocFree
---

# RpcSsSetClientAllocFree function


## -description

The 
<b>RpcSsSetClientAllocFree</b> function enables the memory allocation and release mechanisms used by the client stubs.

## -parameters

### -param ClientAlloc

Memory-allocation function.

### -param ClientFree

Memory-releasing function used with the memory-allocation function specified by <i>pfnAllocate</i>.

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

By overriding the default routines used by the client stub to manage memory, 
<b>RpcSsSetClientAllocFree</b> establishes the memory allocation and memory freeing mechanisms. Note that the default routines are free and malloc, unless the remote call occurs within manager code. In this case, the default memory–management routines are 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>.

Note that when 
<b>RpcSsSetClientAllocFree</b> reclaims the memory resources, it also makes the context handle <b>NULL</b>.

<div class="alert"><b>Note</b>  <b>RpcSsSetClientAllocFree</b> raises exceptions, unlike 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetclientallocfree">RpcSmSetClientAllocFree</a>, which returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetclientallocfree">RpcSmSetClientAllocFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>