---
UID: NF:rpcnsi.RpcNsBindingSelect
title: RpcNsBindingSelect function (rpcnsi.h)
description: The RpcNsBindingSelect function returns a binding handle from a list of compatible binding handles.
helpviewer_keywords: ["RpcNsBindingSelect","RpcNsBindingSelect function [RPC]","_rpc_rpcnsbindingselect","rpc.rpcnsbindingselect","rpcnsi/RpcNsBindingSelect"]
old-location: rpc\rpcnsbindingselect.htm
tech.root: Rpc
ms.assetid: 1acdd266-9ca2-43d4-b677-7c30b4dca4ee
ms.date: 12/05/2018
ms.keywords: RpcNsBindingSelect, RpcNsBindingSelect function [RPC], _rpc_rpcnsbindingselect, rpc.rpcnsbindingselect, rpcnsi/RpcNsBindingSelect
req.header: rpcnsi.h
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsBindingSelect
 - rpcnsi/RpcNsBindingSelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsBindingSelect
---

# RpcNsBindingSelect function


## -description

The 
<b>RpcNsBindingSelect</b> function returns a binding handle from a list of compatible binding handles.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param BindingVec

Pointer to the vector of client-compatible server binding handles from which a binding handle is selected. The returned binding vector no longer references the selected binding handle, which is returned separately in the <i>Binding</i> parameter.

### -param Binding

Pointer to a selected binding handle.

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
<dt><b>RPC_S_NO_MORE_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
No more bindings.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Each time the client calls the 
<b>RpcNsBindingSelect</b> function, the function operation returns another binding handle from the vector.

When all of the binding handles have been returned from the vector, the function returns a status of RPC_S_NO_MORE_BINDINGS and returns a <i>Binding</i> value of <b>NULL</b>.

The <a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> 
	  operation allocates storage for the data referenced by the returned <i>Binding</i> parameter. When a client finishes with the binding handle, it should call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> function to deallocate the storage. Each call to 
<b>RpcNsBindingSelect</b> requires a corresponding call to the 
<b>RpcBindingFree</b> function.

Clients can create their own select routines implementing application-specific selection criteria. In this case, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a> provides access to the fields of a binding.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>