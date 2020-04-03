---
UID: NF:rpcndr.RpcSsFree
title: RpcSsFree function (rpcndr.h)
description: The RpcSsFree function releases memory allocated by RpcSsAllocate.
old-location: rpc\rpcssfree.htm
tech.root: Rpc
ms.assetid: f004ea19-3d1c-485f-99be-da59cbe478d2
ms.date: 12/05/2018
ms.keywords: RpcSsFree, RpcSsFree function [RPC], _rpc_rpcssfree, rpc.rpcssfree, rpcndr/RpcSsFree
f1_keywords:
- rpcndr/RpcSsFree
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Rpcrt4.dll
api_name:
- RpcSsFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcSsFree function


## -description


The 
<b>RpcSsFree</b> function releases memory allocated by 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>.


## -parameters




### -param NodeToFree

Pointer to memory allocated by 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>.


## -remarks



An application uses 
<b>RpcSsFree</b> to free memory that was allocated with 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>. In cases where the stub allocates the memory for the environment, 
<b>RpcSsFree</b> can also be used to release memory. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/memory-management">Memory Management</a>.

Note that the handle of the thread calling 
<b>RpcSsFree</b> must match the handle of the thread that allocated the memory by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>. Use 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a> to pass handles from thread to thread.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a>
 

 

