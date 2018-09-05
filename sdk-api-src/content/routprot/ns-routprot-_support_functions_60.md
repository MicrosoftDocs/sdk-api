---
UID: NS:routprot._SUPPORT_FUNCTIONS_60
title: "_SUPPORT_FUNCTIONS_60"
author: windows-sdk-content
description: The SUPPORT_FUNCTIONS structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.
old-location: rras\support_functions.htm
old-project: RRAS
ms.assetid: c6e1e3a3-2c2a-40ef-965f-554263614bdf
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS structure pointer [RAS], SUPPORT_FUNCTIONS, SUPPORT_FUNCTIONS structure [RAS], SUPPORT_FUNCTIONS_60, _SUPPORT_FUNCTIONS_60, _mpr_support_functions, routprot/PSUPPORT_FUNCTIONS, routprot/SUPPORT_FUNCTIONS, rras.support_functions"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: routprot.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: SUPPORT_FUNCTIONS_60
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - SUPPORT_FUNCTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SUPPORT_FUNCTIONS_60 structure


## -description


The 
<b>SUPPORT_FUNCTIONS</b> structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.


## -struct-fields




### -field _Align8


### -field dwVersion


### -field dwReserved


#### - DemandDialRequest

The routing protocol calls 
<b>DemandDialRequest</b> to initiate a demand-dial connection.

Pointer to the 
<a href="https://msdn.microsoft.com/2951d4d2-fdf5-47ed-b9bc-8268b95b8a6e">DemandDialRequest</a> function provided by the router manager for the routing protocol.



#### ProtocolId

Specifies the identifier of the routing protocol on behalf of which the connection should be established. (Normally, this parameter is the identifier of the calling routing protocol.)



#### InterfaceIndex

Specifies the identifier of the interface for which the connection should be established.


##### - DemandDialRequest.InterfaceIndex

Specifies the identifier of the interface for which the connection should be established.


##### - DemandDialRequest.ProtocolId

Specifies the identifier of the routing protocol on behalf of which the connection should be established. (Normally, this parameter is the identifier of the calling routing protocol.)


#### - MIBEntryCreate

The routing protocol calls 
<b>MIBEntryCreate</b> to execute a Create request of the router manager or a peer protocol DLL. Implement this function to handle SNMP-style requests.

Pointer to the 
<a href="https://msdn.microsoft.com/a65731ec-483d-4e50-aac2-5d55fdac3e3a">MIBEntryCreate</a> function provided by the router manager for the routing protocol.



#### dwRoutingPid

Specifies the identifier of the DLL that should process this request. This parameter may be the identifier of the router manager or the identifier of a routing protocol.



#### InputDataSize

Specifies the size, in bytes, of the data to pass with the Create request.



#### InputData

Pointer to the data to pass with the Create request.


##### - MIBEntryCreate.InputData

Pointer to the data to pass with the Create request.


##### - MIBEntryCreate.InputDataSize

Specifies the size, in bytes, of the data to pass with the Create request.


##### - MIBEntryCreate.dwRoutingPid

Specifies the identifier of the DLL that should process this request. This parameter may be the identifier of the router manager or the identifier of a routing protocol.


#### - MIBEntryDelete

Pointer to the 
<a href="https://msdn.microsoft.com/9108ece9-ecac-44cc-b8cb-79a8381e698b">MIBEntryDelete</a> function provided by the router manager for the routing protocol.


#### - MIBEntryGet

The routing protocol calls 
<b>MIBEntryGet</b> to execute a Get request of the router manager or a peer protocol DLL. Implement this function to handle SNMP-style requests.

Pointer to the 
<a href="https://msdn.microsoft.com/b6807048-5898-4b61-bccf-2644ecdbbda6">MIBEntryGet</a> function provided by the router manager for the routing protocol.



#### dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.



#### InputDataSize

Specifies the size, in bytes, of the data to pass with the Get request.



#### InputData

Pointer to the data to pass with the Get request.



#### OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable contains the size, in bytes, of the output buffer.

On output, this variable contains the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.



#### OutputData

Receives the pointer to a buffer that holds the data from the MIB entry.


##### - MIBEntryGet.InputData

Pointer to the data to pass with the Get request.


##### - MIBEntryGet.InputDataSize

Specifies the size, in bytes, of the data to pass with the Get request.


##### - MIBEntryGet.OutputData

Receives the pointer to a buffer that holds the data from the MIB entry.


##### - MIBEntryGet.OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable contains the size, in bytes, of the output buffer.

On output, this variable contains the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.


##### - MIBEntryGet.dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.


#### - MIBEntryGetFirst

The routing protocol calls 
<b>MIBEntryGetFirst</b> to execute a Get First request of the router manager or a peer protocol DLL. Implement this function to handle SNMP-style requests.

Pointer to the 
<a href="https://msdn.microsoft.com/faa7222b-a862-4395-87e7-203055b34165">MIBEntryGetFirst</a> function provided by the router manager for the routing protocol.



#### dwRoutingPid

Specifies the identifier of the DLL that should process this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.



#### InputDataSize

Specifies the size, in bytes, of the data to pass with the Get First request.



#### InputData

Pointer to the data to pass with the Get First request.



#### OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable specifies the size, in bytes, of the output buffer.

On output, this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.



#### OutputData

Pointer to a buffer that receives the data from the MIB entry.


##### - MIBEntryGetFirst.InputData

Pointer to the data to pass with the Get First request.


##### - MIBEntryGetFirst.InputDataSize

Specifies the size, in bytes, of the data to pass with the Get First request.


##### - MIBEntryGetFirst.OutputData

Pointer to a buffer that receives the data from the MIB entry.


##### - MIBEntryGetFirst.OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable specifies the size, in bytes, of the output buffer.

On output, this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.


##### - MIBEntryGetFirst.dwRoutingPid

Specifies the identifier of the DLL that should process this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.


#### - MIBEntryGetNext

The routing protocol calls 
<b>MIBEntryGetNext</b> to execute a Get Next request of the router manager or a peer protocol DLL. Implement this function to handle SNMP-style requests.

Pointer to the 
<a href="https://msdn.microsoft.com/7332e966-06da-4a25-b57c-6dcc851db98a">MIBEntryGetNext</a> function provided by the router manager for the routing protocol.



#### dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.



#### InputDataSize

Specifies the size, in bytes, of the data to pass with the Get Next request.



#### InputData

Pointer to the data to pass with the Get Next request.



#### OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable specifies the size, in bytes, of the output buffer.

On output this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.



#### OutputData

Pointer to a buffer that  holds the data from the MIB entry.


##### - MIBEntryGetNext.InputData

Pointer to the data to pass with the Get Next request.


##### - MIBEntryGetNext.InputDataSize

Specifies the size, in bytes, of the data to pass with the Get Next request.


##### - MIBEntryGetNext.OutputData

Pointer to a buffer that  holds the data from the MIB entry.


##### - MIBEntryGetNext.OutputDataSize

A pointer to a <b>DWORD</b> variable: 




On input, this variable specifies the size, in bytes, of the output buffer.

On output this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size is not large enough, this variable contains the buffer size required to hold all of the output data.


##### - MIBEntryGetNext.dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.


#### - MIBEntrySet

The routing protocol calls 
<b>MIBEntrySet</b> to execute an SNMP MIB-style Set request of the router manager or a peer protocol DLL.

Pointer to the 
<a href="https://msdn.microsoft.com/f80d0bda-9e03-40ee-8ec5-45c806091d3d">MIBEntrySet</a> function provided by the router manager for the routing protocol.



#### dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.



#### InputDataSize

Specifies the size, in bytes, of the data to pass with the Set request.



#### InputData

Pointer to the data to pass with the Set request.


##### - MIBEntrySet.InputData

Pointer to the data to pass with the Set request.


##### - MIBEntrySet.InputDataSize

Specifies the size, in bytes, of the data to pass with the Set request.


##### - MIBEntrySet.dwRoutingPid

Specifies the identifier of the DLL that  processes this request. This parameter can be the identifier of the router manager or the identifier of a routing protocol.


#### - SetInterfaceReceiveType

The routing protocol calls the 
<b>SetInterfaceReceiveType</b> function to set the receive capability of the specified interface.

Pointer to the 
<a href="https://msdn.microsoft.com/3d350f63-13d6-4ed3-b0be-215b91658e0a">SetInterfaceReceiveType</a> function provided by the router manager for the routing protocol.



#### ProtocolId

Specifies the identifier of the routing protocol that makes the call.



#### InterfaceIndex

Specifies the index of the interface on which to set the receive type.



#### InterfaceReceiveType

Specifies the receive type. This parameter must be one of the following values. 




IR_PROMISCUOUS

IR_PROMISCUOUS_MULTICAST



#### bActivate

Specifies whether to activate the interface.


##### - SetInterfaceReceiveType.InterfaceIndex

Specifies the index of the interface on which to set the receive type.


##### - SetInterfaceReceiveType.InterfaceReceiveType

Specifies the receive type. This parameter must be one of the following values. 




IR_PROMISCUOUS

IR_PROMISCUOUS_MULTICAST


##### - SetInterfaceReceiveType.ProtocolId

Specifies the identifier of the routing protocol that makes the call.


##### - SetInterfaceReceiveType.bActivate

Specifies whether to activate the interface.


#### - ValidateRoute

The routing protocol calls the 
<b>ValidateRoute</b> function to set the route preference and perform other route validation.

Pointer to the 
<a href="https://msdn.microsoft.com/f70bd4bb-8d3c-4408-9e83-4482c5ef8d70">ValidateRoute</a> function provided by the router manager for the routing protocol.



#### ProtocolId

Specifies the identifier of the routing protocol that makes the call.



#### RouteInfo

Pointer to information that describes the route to validate.



#### DestAddress

Pointer to information that describes the destination address. This parameter is optional and can be <b>NULL</b>.


##### - ValidateRoute.DestAddress

Pointer to information that describes the destination address. This parameter is optional and can be <b>NULL</b>.


##### - ValidateRoute.ProtocolId

Specifies the identifier of the routing protocol that makes the call.


##### - ValidateRoute.RouteInfo

Pointer to information that describes the route to validate.


## -see-also




<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a>
 

 

