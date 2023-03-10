---
UID: NF:rpcdce.RpcBindingFree
title: RpcBindingFree function (rpcdce.h)
description: The RpcBindingFree function releases binding-handle resources.
helpviewer_keywords: ["RpcBindingFree","RpcBindingFree function [RPC]","_rpc_rpcbindingfree","rpc.rpcbindingfree","rpcdce/RpcBindingFree"]
old-location: rpc\rpcbindingfree.htm
tech.root: Rpc
ms.assetid: 0f85e64f-b4a6-4982-8df5-88caa0a312f6
ms.date: 12/05/2018
ms.keywords: RpcBindingFree, RpcBindingFree function [RPC], _rpc_rpcbindingfree, rpc.rpcbindingfree, rpcdce/RpcBindingFree
req.header: rpcdce.h
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
 - RpcBindingFree
 - rpcdce/RpcBindingFree
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
 - RpcBindingFree
---

# RpcBindingFree function


## -description

The 
<b>RpcBindingFree</b> function releases binding-handle resources.

## -parameters

### -param Binding

Pointer to the server binding to be freed.

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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcBindingFree</b> function releases memory used by a server binding handle. Referenced binding information that was dynamically created during program execution is released as well. An application calls the 
<b>RpcBindingFree</b> function when it is finished using the binding handle. RPC binding handles must not be freed until all calls using the handle have completed; failure to do so will cause unpredictable results.

Binding handles are dynamically created by calling the following functions:

<ul>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcopy">RpcBindingCopy</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingserverfromclient">RpcBindingServerFromClient</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>
</li>
<li>
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>
</li>
<li>
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a>
</li>
</ul>
If the operation successfully frees the binding, the <i>Binding</i> parameter returns a value of <b>NULL</b>.

<div class="alert"><b>Note</b>  Microsoft RPC supports 
<b>RpcBindingFree</b> only in client applications, or in server applications for binding handles generated with RpcBindingServerFromClient.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcopy">RpcBindingCopy</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>