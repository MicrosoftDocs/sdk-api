---
UID: NF:rpcndr.RpcSmAllocate
title: RpcSmAllocate function (rpcndr.h)
description: The RpcSmAllocate function allocates memory within the RPC stub memory management function and returns a pointer to the allocated memory or NULL.
helpviewer_keywords: ["RpcSmAllocate","RpcSmAllocate function [RPC]","_rpc_rpcsmallocate","rpc.rpcsmallocate","rpcndr/RpcSmAllocate"]
old-location: rpc\rpcsmallocate.htm
tech.root: Rpc
ms.assetid: ca3373fa-8ea4-452e-b2a2-f30eb48fef9d
ms.date: 12/05/2018
ms.keywords: RpcSmAllocate, RpcSmAllocate function [RPC], _rpc_rpcsmallocate, rpc.rpcsmallocate, rpcndr/RpcSmAllocate
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
 - RpcSmAllocate
 - rpcndr/RpcSmAllocate
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
 - RpcSmAllocate
---

# RpcSmAllocate function


## -description

The 
<b>RpcSmAllocate</b> function allocates memory within the RPC stub memory management function and returns a pointer to the allocated memory or <b>NULL</b>.

## -parameters

### -param Size

Size of memory to allocate, in bytes.

### -param pStatus

Pointer to the returned status.

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

The 
<b>RpcSmAllocate</b> routine allows an application to allocate memory within the RPC stub memory–management environment. Prior to calling 
<b>RpcSmAllocate</b>, the memory-management environment must already be established. For memory management called within the stub, the server stub itself may establish the necessary environment. For more information, see 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a>. When using 
<b>RpcSmAllocate</b> to allocate memory not called from the stub, the application must call 
<b>RpcSmEnableAllocate</b> to establish the required memory-management environment.

The 
<b>RpcSmAllocate</b> routine returns a pointer to the allocated memory if the call is successful. Otherwise, a <b>NULL</b> is returned.

When the stub establishes the memory management, it frees any memory allocated by 
<b>RpcSmAllocate</b>. The application can free such memory before returning to the calling stub by calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>.

By contrast, when the application establishes the memory management, it must free any memory allocated. It does so by calling either 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a> or 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate">RpcSmDisableAllocate</a>.

To manage the same memory within the stub memory–management environment, multiple threads can call 
<b>RpcSmAllocate</b> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>. In this case, the threads must share the same stub memory management thread handle. Applications pass thread handles from thread to thread by calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>.

For more information, see 
<a href="/windows/desktop/Rpc/memory-management">Memory Management</a>.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate">RpcSmDisableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>