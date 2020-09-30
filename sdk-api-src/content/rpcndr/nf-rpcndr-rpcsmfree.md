---
UID: NF:rpcndr.RpcSmFree
title: RpcSmFree function (rpcndr.h)
description: The RpcSmFree function releases memory allocated by RpcSmAllocate.
helpviewer_keywords: ["RpcSmFree","RpcSmFree function [RPC]","_rpc_rpcsmfree","rpc.rpcsmfree","rpcndr/RpcSmFree"]
old-location: rpc\rpcsmfree.htm
tech.root: Rpc
ms.assetid: d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65
ms.date: 12/05/2018
ms.keywords: RpcSmFree, RpcSmFree function [RPC], _rpc_rpcsmfree, rpc.rpcsmfree, rpcndr/RpcSmFree
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
 - RpcSmFree
 - rpcndr/RpcSmFree
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
 - RpcSmFree
---

# RpcSmFree function


## -description

The 
<b>RpcSmFree</b> function releases memory allocated by 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>.

## -parameters

### -param NodeToFree

Pointer to memory allocated by 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a> or 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>.

## -returns

The function 
<b>RpcSmFree</b> returns the following value.

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

Applications use 
<b>RpcSmFree</b> to free memory allocated by 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>. In cases where the stub allocates the memory for the application, 
<b>RpcSmFree</b> can also be used to release memory. For more information, see 
<a href="/windows/desktop/Rpc/memory-management">Memory Management</a>.

To improve performance, the 
<b>RpcSmFree</b> function only marks memory for release. Memory is not actually released until your application calls the 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate">RpcSmDisableAllocate</a> function. To release memory immediately, invoke the 
<a href="/windows/desktop/Rpc/the-midl-user-free-function">midl_user_free</a> function.

Note that the handle of the thread calling 
<b>RpcSmFree</b> must match the handle of the thread that allocated the memory by calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate.</a>. Use 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a> to pass handles from thread to thread.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>



<a href="https://msdn.microsoft.com/">midl_user_allocate</a>