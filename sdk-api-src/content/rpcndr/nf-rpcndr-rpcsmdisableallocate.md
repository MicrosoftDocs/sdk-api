---
UID: NF:rpcndr.RpcSmDisableAllocate
title: RpcSmDisableAllocate function (rpcndr.h)
description: The RpcSmDisableAllocate function frees resources and memory within the stub memory—management environment.
helpviewer_keywords: ["RpcSmDisableAllocate","RpcSmDisableAllocate function [RPC]","_rpc_rpcsmdisableallocate","rpc.rpcsmdisableallocate","rpcndr/RpcSmDisableAllocate"]
old-location: rpc\rpcsmdisableallocate.htm
tech.root: Rpc
ms.assetid: 229cab16-eabf-49d3-a61e-3c06e001d0ac
ms.date: 12/05/2018
ms.keywords: RpcSmDisableAllocate, RpcSmDisableAllocate function [RPC], _rpc_rpcsmdisableallocate, rpc.rpcsmdisableallocate, rpcndr/RpcSmDisableAllocate
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
 - RpcSmDisableAllocate
 - rpcndr/RpcSmDisableAllocate
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
 - RpcSmDisableAllocate
---

# RpcSmDisableAllocate function


## -description

The 
<b>RpcSmDisableAllocate</b> function frees resources and memory within the stub memory–management environment.



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
<b>RpcSmDisableAllocate</b> function frees all the resources used by a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a>. It also releases memory allocated by a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a> after the call to 
<b>RpcSmEnableAllocate</b> and marked for deletion by the 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree">RpcSmFree</a> function.

Note that 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a> and 
<b>RpcSmDisableAllocate</b> must be used together as matching pairs.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate">RpcSmAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate">RpcSmEnableAllocate</a>
