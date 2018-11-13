---
UID: NS:rpcndr._MIDL_STUB_DESC
title: "_MIDL_STUB_DESC"
author: windows-sdk-content
description: The MIDL_STUB_DESC structure is a MIDL-generated structure that contains information about the interface stub regarding RPC calls between the client and server.
old-location: rpc\midl_stub_desc.htm
tech.root: rpc
ms.assetid: e3178aaa-a30a-43ba-a78a-a28d6f20fa74
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MIDL_STUB_DESC, MIDL_STUB_DESC structure [RPC], PMIDL_STUB_DESC, PMIDL_STUB_DESC structure pointer [RPC], RPCFLG_HAS_CALLBACK, RPCFLG_HAS_MULTI_SYNTAXES, RPC_INTERFACE_HAS_PIPES, _MIDL_STUB_DESC, rpc.midl_stub_desc, rpcndr/MIDL_STUB_DESC, rpcndr/PMIDL_STUB_DESC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcndr.h
api_name:
 - MIDL_STUB_DESC
product: Windows
targetos: Windows
req.typenames: MIDL_STUB_DESC
req.redist: 
---

# _MIDL_STUB_DESC structure


## -description


The <b>MIDL_STUB_DESC</b> structure is a MIDL-generated structure that contains information about the interface stub regarding RPC calls between the client and server.


## -struct-fields




### -field RpcInterfaceInformation

For a nonobject RPC interface on the server-side, it points to an RPC server interface structure. On the client-side, it points to an RPC client interface structure. It is null for an object interface. 


### -field pfnAllocate

Memory allocation function to be used by the stub. Set to <a href="https://msdn.microsoft.com/">midl_user_allocate</a> for nonobject interface and <a href="https://msdn.microsoft.com/87bfc8ae-62e6-477f-98a7-caf907589b89"> NdrOleAllocate</a> for object interface.  


### -field pfnFree

Memory-free function to be used by the stub. Set to <a href="https://msdn.microsoft.com/b5d8f133-ddd9-4b92-8540-611a03835be0">midl_user_free</a> for nonobject interface and <a href="https://msdn.microsoft.com/c4289448-11bb-40d1-ae63-68521b901796"> NdrOleFree</a> for object interface.  


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

Array of function pointers to expression evaluator functions used to evaluate MIDL complex conformance and varying descriptions. For example, <a href="https://msdn.microsoft.com/1f3f3629-f668-460d-86fd-16ef22449973">size_is</a>(param1 + param2). 


### -field aXmitQuintuple

Array of an array of function pointers for user-defined <a href="https://msdn.microsoft.com/3dd1a242-03ec-49b4-ac96-87ef186e41d2">transmit_as</a> and <a href="https://msdn.microsoft.com/ae44d220-e8f3-47a3-8f5e-a2668ac75411">represent_as</a>  types.


### -field pFormatTypes

Pointer to the type format description.


### -field fCheckBounds

Flag describing the user-specified <a href="https://msdn.microsoft.com/abd3616a-2d2c-4a7d-bf3a-c84a43387894">/error</a> MIDL compiler option.


### -field Version

NDR version required for the stub.


### -field pMallocFreeStruct

Pointer to the MALLOC_FREE_STRUCT structure which contains the allocate and free function pointers. Use if the <a href="https://msdn.microsoft.com/3a232a82-f114-4d8c-8b71-cf8860c77db3">enable_allocate</a> MIDL attribute is specified.


### -field MIDLVersion

Version of the MIDL compiler used to compile the .idl file.


### -field CommFaultOffsets

Array of stack offsets for parameters with <a href="https://msdn.microsoft.com/3ea9ce62-8bd4-40fe-b838-bfebd52b5a15">comm_status</a> or <a href="https://msdn.microsoft.com/">fault_status</a> attributes. 


### -field aUserMarshalQuadruple

Array of an array of function pointers for user-defined <a href="https://msdn.microsoft.com/">user_marshal</a> and <a href="https://msdn.microsoft.com/">wire_marshal</a>  types.


### -field NotifyRoutineTable

Array of notification function pointers for methods with the <a href="https://msdn.microsoft.com/24f9887b-04b7-491a-ab6e-7c078b967fbc">notify</a> or <a href="https://msdn.microsoft.com/a40b7114-d2e3-40c1-a0b1-599428188611">notify_flag</a> attribute specified.


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

