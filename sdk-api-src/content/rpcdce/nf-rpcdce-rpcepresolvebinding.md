---
UID: NF:rpcdce.RpcEpResolveBinding
title: RpcEpResolveBinding function
author: windows-sdk-content
description: The RpcEpResolveBinding function resolves a partially-bound server binding handle into a fully-bound server binding handle.
old-location: rpc\rpcepresolvebinding.htm
old-project: rpc
ms.assetid: 839eefea-f06d-412b-9637-4af01b783121
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcEpResolveBinding, RpcEpResolveBinding function [RPC], _rpc_rpcepresolvebinding, rpc.rpcepresolvebinding, rpcdce/RpcEpResolveBinding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcEpResolveBinding
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcEpResolveBinding function


## -description


The 
<b>RpcEpResolveBinding</b> function resolves a partially-bound server binding handle into a fully-bound server binding handle.


## -parameters




### -param Binding

Partially-bound server binding handle to resolve to a fully-bound server binding handle.


### -param IfSpec

Stub-generated structure specifying the interface of interest.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcEpResolveBinding</b> function to resolve a partially-bound server binding handle into a fully-bound binding handle.

Resolving binding handles requires an interface UUID and an object UUID (which may be nil). The RPC run-time library asks the endpoint-mapping service on the host specified by the <i>Binding</i> parameter to look up an endpoint for a compatible server instance. To find the endpoint, the endpoint-mapping service looks in the endpoint-map database for the interface UUID in the <i>IfSpec</i> parameter and the object UUID in the <i>Binding</i> parameter, if any.

How the resolve-binding operation functions depends on whether the specified binding handle is partially- or fully-bound. When the client specifies a partially-bound handle, the resolve-binding operation has the following possible outcomes:

<ul>
<li>If no compatible server instances are registered in the endpoint-map database, the resolve-binding operation returns the EPT_S_NOT_REGISTERED status code.</li>
<li>If a compatible server instance is registered in the endpoint-map database, the resolve-binding operation returns a fully-bound binding and the RPC_S_OK status code.</li>
</ul>
When the client specifies a fully-bound binding handle, the resolve-binding operation returns the specified binding handle and the RPC_S_OK status code. The resolve-binding operation does not contact the endpoint-mapping service.

In neither the partially- nor the fully-bound binding case does the resolve-binding operation contact a compatible server instance.

<div class="alert"><b>Note</b>  Calling 
<b>RpcEpResolveBinding</b> is not strictly necessary. If an RPC call is made on a partially-bound server binding handle, the RPC run time takes the necessary steps to make the binding into fully bound binding handle. The RPC run time calls 
<b>RpcEpResolveBinding</b>, but does so more efficiently due to additional caching techniques. In Windows XP and Windows 2000, applications have no reason to call 
<b>RpcEpResolveBinding</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a>



<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/eaf132a8-0bc2-4201-945a-76b6c2eab559">RpcEpRegisterNoReplace</a>



<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>



<a href="https://msdn.microsoft.com/093c988a-5d88-45b5-b69a-f26962118fdb">RpcNsBindingImportDone</a>



<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>
 

 

