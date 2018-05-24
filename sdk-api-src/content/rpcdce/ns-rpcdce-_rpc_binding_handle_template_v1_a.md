---
UID: NS:rpcdce._RPC_BINDING_HANDLE_TEMPLATE_V1_A
title: "_RPC_BINDING_HANDLE_TEMPLATE_V1_A"
author: windows-driver-content
description: Contains the basic options with which to create an RPC binding handle.
old-location: rpc\rpc_binding_handle_template_v1.htm
old-project: Rpc
ms.assetid: b5712e0b-1751-4e5f-8000-da2a330da202
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: "*PRPC_BINDING_HANDLE_TEMPLATE_V1_A, RPC_BHT_OBJECT_UUID_VALID, RPC_BINDING_HANDLE_TEMPLATE, RPC_BINDING_HANDLE_TEMPLATE structure [RPC], RPC_BINDING_HANDLE_TEMPLATE_V1, RPC_BINDING_HANDLE_TEMPLATE_V1 structure [RPC], RPC_BINDING_HANDLE_TEMPLATE_V1_A, _RPC_BINDING_HANDLE_TEMPLATE_V1_A, _RPC_BINDING_HANDLE_TEMPLATE_V1_W, ncacn_http, ncacn_ip_tcp, ncacn_np, ncalrpc, rpc.rpc_binding_handle_template_v1, rpcdce/RPC_BINDING_HANDLE_TEMPLATE, rpcdce/RPC_BINDING_HANDLE_TEMPLATE_V1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_BINDING_HANDLE_TEMPLATE_V1_A, *PRPC_BINDING_HANDLE_TEMPLATE_V1_A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rpcdce.h
api_name:
-	RPC_BINDING_HANDLE_TEMPLATE_V1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RPC_BINDING_HANDLE_TEMPLATE_V1_A structure


## -description


The <b>RPC_BINDING_HANDLE_TEMPLATE_V1</b> structure contains the basic options with which to create an RPC binding handle.


## -struct-fields




### -field Version

The version of this structure. For <b>RPC_BINDING_HANDLE_TEMPLATE_V1</b> this must be set to 1.


### -field Flags

Flag values that describe specific properties of the RPC template.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_BHT_OBJECT_UUID_VALID"></a><a id="rpc_bht_object_uuid_valid"></a><dl>
<dt><b>RPC_BHT_OBJECT_UUID_VALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectUuid</b> member contains a valid value. If this flag is not set, then the ObjectUuid member does not contain a valid UUID.

</td>
</tr>
</table>
 


### -field ProtocolSequence

A <a href="https://msdn.microsoft.com/51284532-b0ac-4bf2-b322-91393b2b9dc6">protocol sequence string literal</a> associated with this binding handle.  It can be one of the following values.



##### )



##### )



##### )



##### )


### -field NetworkAddress

Pointer to a string representation of the network address to bind to.


### -field StringEndpoint

Pointer to a string representation of the endpoint to bind to. If a dynamic endpoint is used, set this member to <b>NULL</b>. After the endpoint is resolved, use <a href="https://msdn.microsoft.com/fd4fea9a-067e-4a1b-8be5-867bbe9663c5">RpcBindingToStringBinding</a> to obtain it.


### -field u1


### -field u1.Reserved

Reserved. This member must be set to <b>NULL</b>.


### -field ObjectUuid

The UUID of the remote object. The semantics for this UUID are the same as those for a string binding. After the binding handle is created, call <a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a> to change the UUID as needed.


## -remarks



Fast binding handles are slightly different from "classic" binding handles in the way they are handled during calls to <a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a>. <b>RpcBindingReset</b> is a no-op call for static fast binding handles. For classic binding handles, however, <b>RpcBindingReset</b> converts a static binding handle into a dynamic one to preserve backwards compatibility.

The following table demonstrates the behavior of static and dynamic binding handles with regards to <a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a> and <a href="https://msdn.microsoft.com/839eefea-f06d-412b-9637-4af01b783121">RpcEpResolveBinding</a>.
  <table>
<tr>
<th>Endpoint Type</th>
<th colspan="2">Static</th>
<th colspan="2">Dynamic</th>
</tr>
<tr>
<th>Binding Handle Type</th>
<th>Fast</th>
<th>Classic</th>
<th>Fast</th>
<th>Classic</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a>
</td>
<td>No-op</td>
<td>Converts to dynamic</td>
<td>Removes resolved endpoint if one is present</td>
<td>Removes resolved endpoint if one is present</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/839eefea-f06d-412b-9637-4af01b783121">RpcEpResolveBinding</a>
</td>
<td>No-op</td>
<td>No-op</td>
<td>Resolves endpoint if not previously resolved</td>
<td>Resolves endpoint if not previously resolved</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a>



<a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>



<a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>
 

 

