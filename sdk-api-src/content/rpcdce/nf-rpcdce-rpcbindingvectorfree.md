---
UID: NF:rpcdce.RpcBindingVectorFree
title: RpcBindingVectorFree function (rpcdce.h)
author: windows-sdk-content
description: The RpcBindingVectorFree function frees the binding handles contained in the vector and the vector itself.
old-location: rpc\rpcbindingvectorfree.htm
tech.root: Rpc
ms.assetid: a8af56ae-bacc-497d-b65e-c0a56f3b09de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RpcBindingVectorFree, RpcBindingVectorFree function [RPC], _rpc_rpcbindingvectorfree, rpc.rpcbindingvectorfree, rpcdce/RpcBindingVectorFree
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - RpcBindingVectorFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcBindingVectorFree function


## -description


The 
<b>RpcBindingVectorFree</b> function frees the binding handles contained in the vector and the vector itself.


## -parameters




### -param BindingVector

Pointer to a pointer to a vector of server binding handles. On return, the pointer is set to <b>NULL</b>.


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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was invalid.

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
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcBindingVectorFree</b> function to release the memory used to store a vector of server binding handles. The function frees both the binding handles and the vector itself.

A server obtains a vector of binding handles by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> function. A client obtains a vector of binding handles by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>
 

 

