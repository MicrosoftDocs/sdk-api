---
UID: NS:rpcdce._RPC_BINDING_HANDLE_TEMPLATE_V1_W
title: RPC_BINDING_HANDLE_TEMPLATE_V1_W (rpcdce.h)
description: Contains the basic options with which to create an RPC binding handle. (Unicode)
helpviewer_keywords: ["*PRPC_BINDING_HANDLE_TEMPLATE_V1_W","RPC_BHT_OBJECT_UUID_VALID","RPC_BINDING_HANDLE_TEMPLATE","RPC_BINDING_HANDLE_TEMPLATE structure [RPC]","RPC_BINDING_HANDLE_TEMPLATE_V1","RPC_BINDING_HANDLE_TEMPLATE_V1 structure [RPC]","RPC_BINDING_HANDLE_TEMPLATE_V1_A","RPC_BINDING_HANDLE_TEMPLATE_V1_W","_RPC_BINDING_HANDLE_TEMPLATE_V1_A","_RPC_BINDING_HANDLE_TEMPLATE_V1_W","ncacn_http","ncacn_ip_tcp","ncacn_np","ncalrpc","rpc.rpc_binding_handle_template_v1","rpcdce/RPC_BINDING_HANDLE_TEMPLATE","rpcdce/RPC_BINDING_HANDLE_TEMPLATE_V1"]
old-location: rpc\rpc_binding_handle_template_v1.htm
tech.root: Rpc
ms.assetid: b5712e0b-1751-4e5f-8000-da2a330da202
ms.date: 11/19/2020
ms.keywords: '*PRPC_BINDING_HANDLE_TEMPLATE_V1_W, RPC_BHT_OBJECT_UUID_VALID, RPC_BINDING_HANDLE_TEMPLATE, RPC_BINDING_HANDLE_TEMPLATE structure [RPC], RPC_BINDING_HANDLE_TEMPLATE_V1, RPC_BINDING_HANDLE_TEMPLATE_V1 structure [RPC], RPC_BINDING_HANDLE_TEMPLATE_V1_A, RPC_BINDING_HANDLE_TEMPLATE_V1_W, _RPC_BINDING_HANDLE_TEMPLATE_V1_A, _RPC_BINDING_HANDLE_TEMPLATE_V1_W, ncacn_http, ncacn_ip_tcp, ncacn_np, ncalrpc, rpc.rpc_binding_handle_template_v1, rpcdce/RPC_BINDING_HANDLE_TEMPLATE, rpcdce/RPC_BINDING_HANDLE_TEMPLATE_V1'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_BINDING_HANDLE_TEMPLATE_V1_W, *PRPC_BINDING_HANDLE_TEMPLATE_V1_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_BINDING_HANDLE_TEMPLATE_V1_W
 - rpcdce/_RPC_BINDING_HANDLE_TEMPLATE_V1_W
 - PRPC_BINDING_HANDLE_TEMPLATE_V1_W
 - rpcdce/PRPC_BINDING_HANDLE_TEMPLATE_V1_W
 - RPC_BINDING_HANDLE_TEMPLATE_V1_W
 - rpcdce/RPC_BINDING_HANDLE_TEMPLATE_V1_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_BINDING_HANDLE_TEMPLATE_V1
 - RPC_BINDING_HANDLE_TEMPLATE_V1_A
 - RPC_BINDING_HANDLE_TEMPLATE_V1_W
---

# RPC_BINDING_HANDLE_TEMPLATE_V1_W structure


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

A <a href="/windows/desktop/Rpc/protocol-sequence-constants">protocol sequence string literal</a> associated with this binding handle.  It can be one of the following values.

**ncalrpc** - Specifies local RPC.
**ncacn_ip_tcp** - Specifies RPC over TCP/IP.
**ncacn_np** - Specifies RPC over named pipes.
**ncacn_http** - Specifies RPC over HTTP.

### -field NetworkAddress

Pointer to a string representation of the network address to bind to.

### -field StringEndpoint

Pointer to a string representation of the endpoint to bind to. If a dynamic endpoint is used, set this member to <b>NULL</b>. After the endpoint is resolved, use <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a> to obtain it.

### -field u1

### -field u1.Reserved

Reserved. This member must be set to <b>NULL</b>.

### -field ObjectUuid

The UUID of the remote object. The semantics for this UUID are the same as those for a string binding. After the binding handle is created, call <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a> to change the UUID as needed.


###### - ProtocolSequence.ncacn_http (Specifies RPC over HTTP.)


###### - ProtocolSequence.ncacn_ip_tcp (Specifies RPC over TCP/IP.)


###### - ProtocolSequence.ncacn_np (Specifies RPC over named pipes.)


###### - ProtocolSequence.ncalrpc (Specifies local RPC.)

## -remarks

Fast binding handles are slightly different from "classic" binding handles in the way they are handled during calls to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingreset">RpcBindingReset</a>. <b>RpcBindingReset</b> is a no-op call for static fast binding handles. For classic binding handles, however, <b>RpcBindingReset</b> converts a static binding handle into a dynamic one to preserve backwards compatibility.

The following table demonstrates the behavior of static and dynamic binding handles with regards to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingreset">RpcBindingReset</a> and <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepresolvebinding">RpcEpResolveBinding</a>.
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
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingreset">RpcBindingReset</a>
</td>
<td>No-op</td>
<td>Converts to dynamic</td>
<td>Removes resolved endpoint if one is present</td>
<td>Removes resolved endpoint if one is present</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepresolvebinding">RpcEpResolveBinding</a>
</td>
<td>No-op</td>
<td>No-op</td>
<td>Resolves endpoint if not previously resolved</td>
<td>Resolves endpoint if not previously resolved</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingbind">RpcBindingBind</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a>
