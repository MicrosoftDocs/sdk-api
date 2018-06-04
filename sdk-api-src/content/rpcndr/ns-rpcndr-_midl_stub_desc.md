---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MIDL_STUB_DESC structure


## -description


The <b>MIDL_STUB_DESC</b> structure is a MIDL-generated structure that contains information about the interface stub regarding RPC calls between the client and server.


## -struct-fields




### -field RpcInterfaceInformation

For a nonobject RPC interface on the server-side, it points to an RPC server interface structure. On the client-side, it points to an RPC client interface structure. It is null for an object interface. 


### -field pfnAllocate

Memory allocation function to be used by the stub. Set to <a href="midl.midl_user_allocate_1">midl_user_allocate</a> for nonobject interface and <a href="https://msdn.microsoft.com/87bfc8ae-62e6-477f-98a7-caf907589b89"> NdrOleAllocate</a> for object interface.  


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

Array of function pointers to expression evaluator functions used to evaluate MIDL complex conformance and varying descriptions. For example, <a href="midl.size_is">size_is</a>(param1 + param2). 


### -field aXmitQuintuple

Array of an array of function pointers for user-defined <a href="https://msdn.microsoft.com/3dd1a242-03ec-49b4-ac96-87ef186e41d2">transmit_as</a> and <a href="midl.represent_as">represent_as</a>  types.


### -field pFormatTypes

Pointer to the type format description.


### -field fCheckBounds

Flag describing the user-specified <a href="https://msdn.microsoft.com/abd3616a-2d2c-4a7d-bf3a-c84a43387894">/error</a> MIDL compiler option.


### -field Version

NDR version required for the stub.


### -field pMallocFreeStruct

Pointer to the MALLOC_FREE_STRUCT structure which contains the allocate and free function pointers. Use if the <a href="midl.enable_allocate">enable_allocate</a> MIDL attribute is specified.


### -field MIDLVersion

Version of the MIDL compiler used to compile the .idl file.


### -field CommFaultOffsets

Array of stack offsets for parameters with <a href="midl.comm_status">comm_status</a> or <a href="midl.fault_status">fault_status</a> attributes. 


### -field aUserMarshalQuadruple

Array of an array of function pointers for user-defined <a href="midl.user_marshal">user_marshal</a> and <a href="midl.wire_marshal">wire_marshal</a>  types.


### -field NotifyRoutineTable

Array of notification function pointers for methods with the <a href="midl.notify">notify</a> or <a href="https://msdn.microsoft.com/a40b7114-d2e3-40c1-a0b1-599428188611">notify_flag</a> attribute specified.


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

