---
UID: NF:rpcndr.RpcSsDisableAllocate
title: RpcSsDisableAllocate function (rpcndr.h)
description: The RpcSsDisableAllocate function frees resources and memory within the stub memory—management environment.
helpviewer_keywords: ["RpcSsDisableAllocate","RpcSsDisableAllocate function [RPC]","_rpc_rpcssdisableallocate","rpc.rpcssdisableallocate","rpcndr/RpcSsDisableAllocate"]
old-location: rpc\rpcssdisableallocate.htm
tech.root: Rpc
ms.assetid: 08121380-ff75-4f18-aae4-fdd01e1dfa8b
ms.date: 12/05/2018
ms.keywords: RpcSsDisableAllocate, RpcSsDisableAllocate function [RPC], _rpc_rpcssdisableallocate, rpc.rpcssdisableallocate, rpcndr/RpcSsDisableAllocate
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
 - RpcSsDisableAllocate
 - rpcndr/RpcSsDisableAllocate
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
 - RpcSsDisableAllocate
---

# RpcSsDisableAllocate function


## -description

The 
<b>RpcSsDisableAllocate</b> function frees resources and memory within the stub memory–management environment.



## -returns

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcSsDisableAllocate</b> frees all the resources used by a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssenableallocate">RpcSsEnableAllocate</a>. It also releases memory that was allocated by a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a> after the call to 
<b>RpcSsEnableAllocate</b>.


<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssenableallocate">RpcSsEnableAllocate</a> and 
<b>RpcSsDisableAllocate</b> must be used together as matching pairs.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate">RpcSmDisableAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssenableallocate">RpcSsEnableAllocate</a>
