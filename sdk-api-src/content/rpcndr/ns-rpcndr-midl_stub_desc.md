---
UID: NS:rpcndr._MIDL_STUB_DESC
title: MIDL_STUB_DESC (rpcndr.h)
description: The MIDL_STUB_DESC structure is a MIDL-generated structure that contains information about the interface stub regarding RPC calls between the client and server.
helpviewer_keywords: ["MIDL_STUB_DESC","MIDL_STUB_DESC structure [RPC]","PMIDL_STUB_DESC","PMIDL_STUB_DESC structure pointer [RPC]","RPCFLG_HAS_CALLBACK","RPCFLG_HAS_MULTI_SYNTAXES","RPC_INTERFACE_HAS_PIPES","rpc.midl_stub_desc","rpcndr/MIDL_STUB_DESC","rpcndr/PMIDL_STUB_DESC"]
old-location: rpc\midl_stub_desc.htm
tech.root: Rpc
ms.assetid: e3178aaa-a30a-43ba-a78a-a28d6f20fa74
ms.date: 12/05/2018
ms.keywords: MIDL_STUB_DESC, MIDL_STUB_DESC structure [RPC], PMIDL_STUB_DESC, PMIDL_STUB_DESC structure pointer [RPC], RPCFLG_HAS_CALLBACK, RPCFLG_HAS_MULTI_SYNTAXES, RPC_INTERFACE_HAS_PIPES, rpc.midl_stub_desc, rpcndr/MIDL_STUB_DESC, rpcndr/PMIDL_STUB_DESC
req.header: rpcndr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIDL_STUB_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIDL_STUB_DESC
 - rpcndr/_MIDL_STUB_DESC
 - MIDL_STUB_DESC
 - rpcndr/MIDL_STUB_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcndr.h
api_name:
 - MIDL_STUB_DESC
---

# MIDL_STUB_DESC structure


## -description

The <b>MIDL_STUB_DESC</b> structure is a MIDL-generated structure that contains information about the interface stub regarding RPC calls between the client and server.

## -struct-fields

### -field RpcInterfaceInformation

For a nonobject RPC interface on the server-side, it points to an RPC server interface structure. On the client-side, it points to an RPC client interface structure. It is null for an object interface.

### -field pfnAllocate

Memory allocation function to be used by the stub. Set to <a href="https://msdn.microsoft.com/">midl_user_allocate</a> for nonobject interface and <a href="/windows/desktop/api/rpcndr/nf-rpcndr-ndroleallocate"> NdrOleAllocate</a> for object interface.

### -field pfnFree

Memory-free function to be used by the stub. Set to <a href="/windows/desktop/Midl/midl-user-free-1">midl_user_free</a> for nonobject interface and <a href="/windows/desktop/api/rpcndr/nf-rpcndr-ndrolefree"> NdrOleFree</a> for object interface.

### -field IMPLICIT_HANDLE_INFO

The union contains one of the following handles.

### -field IMPLICIT_HANDLE_INFO.pAutoHandle

Pointer to the implicit auto handle for the RPC call.

### -field IMPLICIT_HANDLE_INFO.pPrimitiveHandle

Pointer to the implicit primitive handle for the RPC call.

### -field IMPLICIT_HANDLE_INFO.pGenericBindingInfo

Pointer to the information about the implicit generic handle.

### -field apfnNdrRundownRoutines

Array of context handle rundown functions.

### -field aGenericBindingRoutinePairs

Array of function pointers to bind and unbind function pairs for the implicit generic handle.

### -field apfnExprEval

Array of function pointers to expression evaluator functions used to evaluate MIDL complex conformance and varying descriptions. For example, <a href="/windows/desktop/Midl/size-is">size_is</a>(param1 + param2).

### -field aXmitQuintuple

Array of an array of function pointers for user-defined <a href="/windows/desktop/Midl/transmit-as">transmit_as</a> and <a href="https://msdn.microsoft.com/">represent_as</a>  types.

### -field pFormatTypes

Pointer to the type format description.

### -field fCheckBounds

Flag describing the user-specified <a href="/windows/desktop/Midl/-error">/error</a> MIDL compiler option.

### -field Version

NDR version required for the stub.

### -field pMallocFreeStruct

Pointer to the MALLOC_FREE_STRUCT structure which contains the allocate and free function pointers. Use if the <a href="/windows/desktop/Midl/enable-allocate">enable_allocate</a> MIDL attribute is specified.

### -field MIDLVersion

Version of the MIDL compiler used to compile the .idl file.

### -field CommFaultOffsets

Array of stack offsets for parameters with <a href="/windows/desktop/Midl/comm-status">comm_status</a> or <a href="https://msdn.microsoft.com/">fault_status</a> attributes.

### -field aUserMarshalQuadruple

Array of an array of function pointers for user-defined <a href="/windows/desktop/Midl/user-marshal">user_marshal</a> and <a href="/windows/desktop/Midl/wire-marshal">wire_marshal</a>  types.

### -field NotifyRoutineTable

Array of notification function pointers for methods with the <a href="/windows/desktop/Midl/notify">notify</a> or <a href="/windows/desktop/Midl/notify-flag">notify_flag</a> attribute specified.

### -field mFlags

Flag describing the attributes of the stub

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPCFLG_HAS_MULTI_SYNTAXES"></a><a id="rpcflg_has_multi_syntaxes"></a><dl>
<dt><b>RPCFLG_HAS_MULTI_SYNTAXES</b></dt>
</dl>
</td>
<td width="60%">
Set if the stub supports multiple transfer syntaxes.

</td>
</tr>
<tr>
<td width="40%"><a id="RPCFLG_HAS_CALLBACK"></a><a id="rpcflg_has_callback"></a><dl>
<dt><b>RPCFLG_HAS_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Set if the interface contains callback  functions.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_INTERFACE_HAS_PIPES"></a><a id="rpc_interface_has_pipes"></a><dl>
<dt><b>RPC_INTERFACE_HAS_PIPES</b></dt>
</dl>
</td>
<td width="60%">
Set if the interface contains a method that uses pipes.

</td>
</tr>
</table>

### -field CsRoutineTables

Unused.

### -field ProxyServerInfo

### -field pExprInfo

 




#### - Reserved4

Unused.


#### - Reserved5

Unused.
