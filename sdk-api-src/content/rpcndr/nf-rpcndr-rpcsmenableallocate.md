---
UID: NF:rpcndr.RpcSmEnableAllocate
title: RpcSmEnableAllocate function (rpcndr.h)
description: The RpcSmEnableAllocate function establishes the stub memory—management environment.
helpviewer_keywords: ["RpcSmEnableAllocate","RpcSmEnableAllocate function [RPC]","_rpc_rpcsmenableallocate","rpc.rpcsmenableallocate","rpcndr/RpcSmEnableAllocate"]
old-location: rpc\rpcsmenableallocate.htm
tech.root: Rpc
ms.assetid: a0b144fc-873e-4884-b842-ac0eea84487b
ms.date: 12/05/2018
ms.keywords: RpcSmEnableAllocate, RpcSmEnableAllocate function [RPC], _rpc_rpcsmenableallocate, rpc.rpcsmenableallocate, rpcndr/RpcSmEnableAllocate
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
 - RpcSmEnableAllocate
 - rpcndr/RpcSmEnableAllocate
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
 - RpcSmEnableAllocate
---

# RpcSmEnableAllocate function


## -description

The 
<b>RpcSmEnableAllocate</b> function establishes the stub memory–management environment.



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

In cases where the stub memory management is not enabled by the server stub itself, applications call 
<b>RpcSmEnableAllocate</b> to establish the stub memory–management environment. This environment must be established prior to making a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>. In OSF-compatibility (<b>/osf</b>) mode, for server manager code called from the stub, the memory-management environment may be established by the server stub itself by using pointer manipulation or the 
<a href="/windows/desktop/Midl/enable-allocate">enable_allocate</a> attribute. In default (Microsoft-extended) mode, the environment is established only upon request by using the 
<a href="/windows/desktop/Midl/enable-allocate">enable_allocate</a> attribute. Otherwise, call 
<b>RpcSmEnableAllocate</b> before calling 
<b>RpcSmAllocate</b>. For more information, see 
<a href="/windows/desktop/Rpc/memory-management">Memory Management</a>, 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a>, and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate">RpcSmDisableAllocate</a>
