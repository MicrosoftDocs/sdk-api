---
UID: NF:rpcnsi.RpcNsBindingSelect
title: RpcNsBindingSelect function
author: windows-driver-content
description: The RpcNsBindingSelect function returns a binding handle from a list of compatible binding handles.
old-location: rpc\rpcnsbindingselect.htm
old-project: Rpc
ms.assetid: 1acdd266-9ca2-43d4-b677-7c30b4dca4ee
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcNsBindingSelect, RpcNsBindingSelect function [RPC], _rpc_rpcnsbindingselect, rpc.rpcnsbindingselect, rpcnsi/RpcNsBindingSelect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcns4.dll
api_name:
-	RpcNsBindingSelect
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Each time the client calls the 
<b>RpcNsBindingSelect</b> function, the function operation returns another binding handle from the vector.

When all of the binding handles have been returned from the vector, the function returns a status of RPC_S_NO_MORE_BINDINGS and returns a <i>Binding</i> value of <b>NULL</b>.

The <a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> 
	  operation allocates storage for the data referenced by the returned <i>Binding</i> parameter. When a client finishes with the binding handle, it should call the 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> function to deallocate the storage. Each call to 
<b>RpcNsBindingSelect</b> requires a corresponding call to the 
<b>RpcBindingFree</b> function.

Clients can create their own select routines implementing application-specific selection criteria. In this case, 
<a href="https://msdn.microsoft.com/c55d0259-e251-42d0-8565-ce71ab3bb59c">RpcStringBindingParse</a> provides access to the fields of a binding.




## -see-also




<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>



<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>



<a href="https://msdn.microsoft.com/c55d0259-e251-42d0-8565-ce71ab3bb59c">RpcStringBindingParse</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>
 

 

