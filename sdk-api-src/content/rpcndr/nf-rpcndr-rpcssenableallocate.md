---
UID: NF:rpcndr.RpcSsEnableAllocate
title: RpcSsEnableAllocate function (rpcndr.h)
description: The RpcSsEnableAllocate function establishes the stub memory—management environment.
helpviewer_keywords: ["RpcSsEnableAllocate","RpcSsEnableAllocate function [RPC]","_rpc_rpcssenableallocate","rpc.rpcssenableallocate","rpcndr/RpcSsEnableAllocate"]
old-location: rpc\rpcssenableallocate.htm
tech.root: Rpc
ms.assetid: 18060ed2-2250-47c7-8579-238edea44c66
ms.date: 12/05/2018
ms.keywords: RpcSsEnableAllocate, RpcSsEnableAllocate function [RPC], _rpc_rpcssenableallocate, rpc.rpcssenableallocate, rpcndr/RpcSsEnableAllocate
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
 - RpcSsEnableAllocate
 - rpcndr/RpcSsEnableAllocate
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
 - RpcSsEnableAllocate
---

# RpcSsEnableAllocate function


## -description

The 
<b>RpcSsEnableAllocate</b> function establishes the stub memory–management environment.



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

In cases where the stub memory management is not enabled by the stub itself, an application calls 
<b>RpcSsEnableAllocate</b> to establish the stub memory–management environment. This environment must be established prior to making a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>. For server manager code called from the stub, the memory-management environment is usually established by the stub itself. Otherwise, call 
<b>RpcSsEnableAllocate</b> before calling 
<b>RpcSsAllocate</b>. For more information, see 
<a href="/windows/desktop/Rpc/memory-management">Memory Management</a>, 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a>, and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a>.

<div class="alert"><b>Note</b>  The 
<b>RpcSsEnableAllocate</b> function raises exceptions, while the 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a> function returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdisableallocate">RpcSsDisableAllocate</a>
