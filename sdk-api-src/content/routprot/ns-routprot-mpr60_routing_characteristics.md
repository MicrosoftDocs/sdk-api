---
UID: NS:routprot._MPR60_ROUTING_CHARACTERISTICS
title: MPR60_ROUTING_CHARACTERISTICS (routprot.h)
description: The MPR_ROUTING_CHARACTERISTICS structure contains information used to register routing protocols with the router manager.M
helpviewer_keywords: ["*PMPR_ROUTING_CHARACTERISTICS","DEMAND_UPDATE_ROUTES","DEMAND_UPDATE_SERVICES","MPR50_ROUTING_CHARACTERISTICS","MPR50_ROUTING_CHARACTERISTICS structure [RAS]","MPR60_ROUTING_CHARACTERISTICS","MPR_ROUTING_CHARACTERISTICS","MPR_ROUTING_CHARACTERISTICS structure [RAS]","PMPR_ROUTING_CHARACTERISTICS","PMPR_ROUTING_CHARACTERISTICS structure pointer [RAS]","ROUTING","SERVICES","_mpr_mpr_routing_characteristics","routprot/MPR_ROUTING_CHARACTERISTICS","routprot/PMPR_ROUTING_CHARACTERISTICS","rras.mpr_routing_characteristics"]
old-location: rras\mpr_routing_characteristics.htm
tech.root: RRAS
ms.assetid: 7046c4c2-b0bd-4459-b361-e46ce876823f
ms.date: 12/05/2018
ms.keywords: '*PMPR_ROUTING_CHARACTERISTICS, DEMAND_UPDATE_ROUTES, DEMAND_UPDATE_SERVICES, MPR50_ROUTING_CHARACTERISTICS, MPR50_ROUTING_CHARACTERISTICS structure [RAS], MPR60_ROUTING_CHARACTERISTICS, MPR_ROUTING_CHARACTERISTICS, MPR_ROUTING_CHARACTERISTICS structure [RAS], PMPR_ROUTING_CHARACTERISTICS, PMPR_ROUTING_CHARACTERISTICS structure pointer [RAS], ROUTING, SERVICES, _mpr_mpr_routing_characteristics, routprot/MPR_ROUTING_CHARACTERISTICS, routprot/PMPR_ROUTING_CHARACTERISTICS, rras.mpr_routing_characteristics'
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
req.typenames: MPR60_ROUTING_CHARACTERISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR60_ROUTING_CHARACTERISTICS
 - routprot/_MPR60_ROUTING_CHARACTERISTICS
 - MPR60_ROUTING_CHARACTERISTICS
 - routprot/MPR60_ROUTING_CHARACTERISTICS
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
 - MPR50_ROUTING_CHARACTERISTICS
---

# MPR60_ROUTING_CHARACTERISTICS structure


## -description

The 
<b>MPR_ROUTING_CHARACTERISTICS</b> structure contains information used to register routing protocols with the router manager.

## -struct-fields

### -field dwVersion

On input, specifies the version of RRAS currently running. 




On output, the routing protocol should specify the version of RRAS that it requires.

The symbol MS_ROUTER_VERSION in the header file Routprot.h is defined to be the RRAS version for a given implementation.

### -field dwProtocolId

Specifies the routing protocol that the router manager requests the DLL to register. (A common name space is used for all protocol families.)

### -field fSupportedFunctionality

On input, specifies the functionality that the router manager supports. 




On output, the routing protocol should reset these flags to indicate the subset of functionality that it supports.

This parameter is a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ROUTING"></a><a id="routing"></a><dl>
<dt><b>ROUTING</b></dt>
</dl>
</td>
<td width="60%">
The protocol participates in multi-protocol routing by importing routing table manager APIs. There is one routing table manager that maintains a table for each protocol family (such as IP and IPX).
							

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICES"></a><a id="services"></a><dl>
<dt><b>SERVICES</b></dt>
</dl>
</td>
<td width="60%">
The protocol assumes responsibility for managing services (such as IPX SAP), and provides Service Table Management APIs.

</td>
</tr>
<tr>
<td width="40%"><a id="DEMAND_UPDATE_ROUTES"></a><a id="demand_update_routes"></a><dl>
<dt><b>DEMAND_UPDATE_ROUTES</b></dt>
</dl>
</td>
<td width="60%">
The protocol is able to perform autostatic updates of routes when requested by the router manager.

</td>
</tr>
<tr>
<td width="40%"><a id="DEMAND_UPDATE_SERVICES"></a><a id="demand_update_services"></a><dl>
<dt><b>DEMAND_UPDATE_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
The protocol is able to perform autostatic updates of services when requested by the router manager.

</td>
</tr>
</table>

### -field pfnStartProtocol

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pstart_protocol">StartProtocol</a> function for this routing protocol.

### -field pfnStartComplete

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pstart_complete">StartComplete</a> function for this routing protocol.

### -field pfnStopProtocol

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pstop_protocol">StopProtocol</a> function for this routing protocol.

### -field pfnGetGlobalInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_global_info">GetGlobalInfo</a> function for this routing protocol.

### -field pfnSetGlobalInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pset_global_info">SetGlobalInfo</a> function for this routing protocol.

### -field pfnQueryPower

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pquery_power">QueryPower</a> function for this routing protocol.

### -field pfnSetPower

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pset_power">SetPower</a> function for this routing protocol.

### -field pfnAddInterface

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-padd_interface">AddInterface</a> function for this routing protocol.

### -field pfnDeleteInterface

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pdelete_interface">DeleteInterface</a> function for this routing protocol.

### -field pfnInterfaceStatus

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pinterface_status">InterfaceStatus</a> function for this routing protocol.

### -field pfnGetInterfaceInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_interface_info">GetInterfaceInfo</a> function for this routing protocol.

### -field pfnSetInterfaceInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pset_interface_info">SetInterfaceInfo</a> function for this routing protocol.

### -field pfnGetEventMessage

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a> function for this routing protocol.

### -field pfnUpdateRoutes

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pdo_update_routes">DoUpdateRoutes</a> function for this routing protocol.

### -field pfnConnectClient

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pconnect_client">ConnectClient</a> function for this routing protocol.

### -field pfnDisconnectClient

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pdisconnect_client">DisconnectClient</a> function for this routing protocol.

### -field pfnGetNeighbors

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_neighbors">GetNeighbors</a> function for this routing protocol.

### -field pfnGetMfeStatus

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_mfe_status">GetMfeStatus</a> function for this routing protocol.

### -field pfnMibCreateEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_create">MibCreate</a> function for this routing protocol.

### -field pfnMibDeleteEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_delete">MibDelete</a> function for this routing protocol.

### -field pfnMibGetEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get">MibGet</a> function for this routing protocol.

### -field pfnMibSetEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_set">MibSet</a> function for this routing protocol.

### -field pfnMibGetFirstEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_first">MibGetFirst</a> function for this routing protocol.

### -field pfnMibGetNextEntry

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_next">MibGetNext</a> function for this routing protocol.

### -field pfnMibSetTrapInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_set_trap_info">MibSetTrapInfo</a> function for this routing protocol.

### -field pfnMibGetTrapInfo

Pointer to an implementation of the 
<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_trap_info">MibGetTrapInfo</a> function for this routing protocol.

### -field pfnProtocolAction

### -field pfnGetStatistics

### -field pfnGetRoutingDomainGlobalInfo

### -field pfnSetRoutingDomainGlobalInfo

### -field pfnBufferFree

## -remarks

Most of the members of this structure are pointers to functions implemented in the routing protocol DLL. The routing protocol fills in the address values for these pointers during a call to the 
<a href="/windows/desktop/api/routprot/nc-routprot-pregister_protocol">RegisterProtocol</a> function.

For a complete description of a particular function pointed to by one of the structure members, see the reference page for that function.

## -see-also

<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pregister_protocol">RegisterProtocol</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-structures">Routing Protocol Interface Structures</a>
