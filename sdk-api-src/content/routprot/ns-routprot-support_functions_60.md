---
UID: NS:routprot._SUPPORT_FUNCTIONS_60
title: SUPPORT_FUNCTIONS_60 (routprot.h)
description: The SUPPORT_FUNCTIONS structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.
helpviewer_keywords: ["*PSUPPORT_FUNCTIONS","PSUPPORT_FUNCTIONS","PSUPPORT_FUNCTIONS structure pointer [RAS]","SUPPORT_FUNCTIONS","SUPPORT_FUNCTIONS structure [RAS]","SUPPORT_FUNCTIONS_60","_mpr_support_functions","routprot/PSUPPORT_FUNCTIONS","routprot/SUPPORT_FUNCTIONS","rras.support_functions"]
old-location: rras\support_functions.htm
tech.root: RRAS
ms.assetid: c6e1e3a3-2c2a-40ef-965f-554263614bdf
ms.date: 12/05/2018
ms.keywords: '*PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS structure pointer [RAS], SUPPORT_FUNCTIONS, SUPPORT_FUNCTIONS structure [RAS], SUPPORT_FUNCTIONS_60, _mpr_support_functions, routprot/PSUPPORT_FUNCTIONS, routprot/SUPPORT_FUNCTIONS, rras.support_functions'
req.header: routprot.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SUPPORT_FUNCTIONS_60
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SUPPORT_FUNCTIONS_60
 - routprot/_SUPPORT_FUNCTIONS_60
 - SUPPORT_FUNCTIONS_60
 - routprot/SUPPORT_FUNCTIONS_60
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - SUPPORT_FUNCTIONS
---

# SUPPORT_FUNCTIONS_60 structure


## -description

The 
<b>SUPPORT_FUNCTIONS</b> structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.

## -struct-fields

### -field _Align8

### -field dwVersion

### -field dwReserved

### -field BOOL

TBD

### -field DWORD

TBD 




#### - DemandDialRequest

The routing protocol calls 
<b>DemandDialRequest</b> to initiate a demand-dial connection.

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa373924(v=vs.85)">DemandDialRequest</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa374538(v=vs.85)">MIBEntryCreate</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa374539(v=vs.85)">MIBEntryDelete</a> function provided by the router manager for the routing protocol.


#### - MIBEntryGet

The routing protocol calls 
<b>MIBEntryGet</b> to execute a Get request of the router manager or a peer protocol DLL. Implement this function to handle SNMP-style requests.

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa374540(v=vs.85)">MIBEntryGet</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa374541(v=vs.85)">MIBEntryGetFirst</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa374542(v=vs.85)">MIBEntryGetNext</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa374543(v=vs.85)">MIBEntrySet</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa382181(v=vs.85)">SetInterfaceReceiveType</a> function provided by the router manager for the routing protocol.



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
<a href="/previous-versions/windows/desktop/legacy/aa382342(v=vs.85)">ValidateRoute</a> function provided by the router manager for the routing protocol.



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

<a href="/windows/desktop/api/routprot/nc-routprot-pstart_protocol">StartProtocol</a>