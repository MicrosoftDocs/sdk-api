---
UID: NF:rpcndr.RpcSmDestroyClientContext
title: RpcSmDestroyClientContext function (rpcndr.h)
description: The RpcSmDestroyClientContext function reclaims the client memory resources for a context handle and makes the context handle NULL.
helpviewer_keywords: ["RpcSmDestroyClientContext","RpcSmDestroyClientContext function [RPC]","_rpc_rpcsmdestroyclientcontext","rpc.rpcsmdestroyclientcontext","rpcndr/RpcSmDestroyClientContext"]
old-location: rpc\rpcsmdestroyclientcontext.htm
tech.root: Rpc
ms.assetid: ae886740-09e9-46a1-aa62-5dbcf6abab36
ms.date: 12/05/2018
ms.keywords: RpcSmDestroyClientContext, RpcSmDestroyClientContext function [RPC], _rpc_rpcsmdestroyclientcontext, rpc.rpcsmdestroyclientcontext, rpcndr/RpcSmDestroyClientContext
f1_keywords:
- rpcndr/RpcSmDestroyClientContext
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
- RpcSmDestroyClientContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcSmDestroyClientContext function


## -description


The 
<b>RpcSmDestroyClientContext</b> function reclaims the client memory resources for a context handle and makes the context handle <b>NULL</b>.


## -parameters




### -param ContextHandle

Context handle that can no longer be used. The handle is set to <b>NULL</b> before <b>RpcSMDestroyClientContext</b> returns.


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
<dt><b>RPC_X_SS_CONTEXT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Client applications use 
<b>RpcSmDestroyClientContext</b> to reclaim resources from an inactive context handle. Applications can call 
<b>RpcSmDestroyClientContext</b> after a communications error makes the context handle unusable. The 
<b>RpcSmDestroyClientContext</b> function provides the same functionality as the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext">RpcSsDestroyClientContext</a> function.

This function does not invoke the server's context handle run-down process.

When 
<b>RpcSmDestroyClientContext</b> reclaims the memory resources, it also makes the context handle <b>NULL</b>. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/using-context-handles">Using Context Handles</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext">RpcSsDestroyClientContext</a>
 

 

