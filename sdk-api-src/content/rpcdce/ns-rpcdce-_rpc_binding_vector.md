---
UID: NS:rpcdce._RPC_BINDING_VECTOR
title: "_RPC_BINDING_VECTOR"
author: windows-driver-content
description: The RPC_BINDING_VECTOR structure contains a list of binding handles over which a server application can receive remote procedure calls.
old-location: rpc\rpc_binding_vector.htm
old-project: Rpc
ms.assetid: 16a0a595-ed4f-4871-a1a3-268c6bed0305
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RPC_BINDING_VECTOR, RPC_BINDING_VECTOR structure [RPC], _RPC_BINDING_VECTOR, _rpc_rpc_binding_vector, rpc.rpc_binding_vector, rpcdce/RPC_BINDING_VECTOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: RPC_BINDING_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rpcdce.h
api_name:
-	RPC_BINDING_VECTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _RPC_BINDING_VECTOR structure


## -description


The 
<b>RPC_BINDING_VECTOR</b> structure contains a list of binding handles over which a server application can receive remote procedure calls.


## -struct-fields




### -field Count

Number of binding handles present in the binding-handle array <b>BindingH</b>.


### -field BindingH

Array of binding handles that contains <b>Count</b> elements.


## -remarks



The binding vector contains a count member (<b>Count</b>), followed by an array of binding-handle (<b>BindingH</b>) elements.

The RPC run-time library creates binding handles when a server application registers protocol sequences. To obtain a binding vector, a server application calls 
<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a>.

A client application obtains a binding vector of compatible servers from the name-service database by calling 
<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>.

In both routines, the RPC run-time library allocates memory for the binding vector. An application calls 
<a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a> to free the binding vector.

To remove an individual binding handle from the vector, the application must set the value in the vector to <b>NULL</b>. When setting a vector element to <b>NULL</b>, the application must:

<ul>
<li>Free the individual binding.</li>
<li>Not change the value of <b>Count</b>.</li>
</ul>
Calling 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> allows an application to free all binding handles in the vector.




## -see-also




<a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a>



<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>



<a href="https://msdn.microsoft.com/bb0485fc-0b25-4fc0-9a18-921a9de428ce">RpcEpUnregister</a>



<a href="https://msdn.microsoft.com/c89d04d7-f607-48cc-8cb6-b6aebab41671">RpcNsBindingExport</a>



<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>



<a href="https://msdn.microsoft.com/1acdd266-9ca2-43d4-b677-7c30b4dca4ee">RpcNsBindingSelect</a>



<a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a>
 

 

