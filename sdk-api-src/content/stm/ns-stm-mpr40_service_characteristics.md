---
UID: NS:stm._MPR40_SERVICE_CHARACTERISTICS
title: MPR40_SERVICE_CHARACTERISTICS (stm.h)
description: The MPR40_SERVICE_CHARACTERISTICS (stm.h) structure contains information used to register a routing protocol with the router manager.
helpviewer_keywords: ["*PMPR_SERVICE_CHARACTERISTICS","DEMAND_UPDATE_ROUTES","DEMAND_UPDATE_SERVICES","MPR40_SERVICE_CHARACTERISTICS","MPR_SERVICE_CHARACTERISTICS","MPR_SERVICE_CHARACTERISTICS structure [RAS]","PMPR_SERVICE_CHARACTERISTICS","PMPR_SERVICE_CHARACTERISTICS structure pointer [RAS]","ROUTING","SERVICES","_mpr_mpr_service_characteristics","routprot/MPR_SERVICE_CHARACTERISTICS","routprot/PMPR_SERVICE_CHARACTERISTICS","rras.mpr_service_characteristics","stm/MPR_SERVICE_CHARACTERISTICS","stm/PMPR_SERVICE_CHARACTERISTICS"]
old-location: rras\mpr_service_characteristics.htm
tech.root: RRAS
ms.assetid: 92a117ae-3a5f-4702-a936-8e23bc575763
ms.date: 08/15/2022
ms.keywords: '*PMPR_SERVICE_CHARACTERISTICS, DEMAND_UPDATE_ROUTES, DEMAND_UPDATE_SERVICES, MPR40_SERVICE_CHARACTERISTICS, MPR_SERVICE_CHARACTERISTICS, MPR_SERVICE_CHARACTERISTICS structure [RAS], PMPR_SERVICE_CHARACTERISTICS, PMPR_SERVICE_CHARACTERISTICS structure pointer [RAS], ROUTING, SERVICES, _mpr_mpr_service_characteristics, routprot/MPR_SERVICE_CHARACTERISTICS, routprot/PMPR_SERVICE_CHARACTERISTICS, rras.mpr_service_characteristics, stm/MPR_SERVICE_CHARACTERISTICS, stm/PMPR_SERVICE_CHARACTERISTICS'
req.header: stm.h
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
req.typenames: MPR40_SERVICE_CHARACTERISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR40_SERVICE_CHARACTERISTICS
 - stm/_MPR40_SERVICE_CHARACTERISTICS
 - MPR40_SERVICE_CHARACTERISTICS
 - stm/MPR40_SERVICE_CHARACTERISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
 - Stm.h
api_name:
 - MPR_SERVICE_CHARACTERISTICS
---

# MPR40_SERVICE_CHARACTERISTICS structure


## -description

The 
<b>MPR_SERVICE_CHARACTERISTICS</b> structure contains information used to register a routing protocol with the router manager.

## -struct-fields

### -field dwVersion

On input, specifies the version of RRAS currently running. 




On output, the routing protocol should specify the version of RRAS that it requires.

The symbol MS_ROUTER_VERSION in the header file Routprot.h is defined to be the RRAS version for a given implementation.

### -field dwProtocolId

Specifies the routing protocol that the router manager requests the DLL to register. (A common name space is used for all protocol families.)

### -field fSupportedFunctionality

On input, specifies the functionality that the router manager supports. 




On output, the routing protocol should reset these flags to indicate the subset of functionality that it supports. If this routing protocol does not provide services, <b>fSupportedFunctionality</b> should be zero.

This parameter is one or more of the following values.

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

### -field pfnIsService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pis_service">IsService</a> function for this routing protocol.

### -field pfnUpdateServices

### -field pfnCreateServiceEnumerationHandle

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pcreate_service_enumeration_handle">CreateServiceEnumerationHandle</a> function for this routing protocol.

### -field pfnEnumerateGetNextService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-penumerate_get_next_service">EnumerateGetNextService</a> function for this routing protocol.

### -field pfnCloseServiceEnumerationHandle

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pclose_service_enumeration_handle">CloseServiceEnumerationHandle</a> function for this routing protocol.

### -field pfnGetServiceCount

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pget_service_count">GetServiceCount</a> function for this routing protocol.

### -field pfnCreateStaticService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pcreate_static_service">CreateStaticService</a> function for this routing protocol.

### -field pfnDeleteStaticService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pdelete_static_service">DeleteStaticService</a> function for this routing protocol.

### -field pfnBlockConvertServicesToStatic

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pblock_convert_services_to_static">BlockConvertServicesToStatic</a> function for this routing protocol.

### -field pfnBlockDeleteStaticServices

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pblock_delete_static_services">BlockDeleteStaticServices</a> function for this routing protocol.

### -field pfnGetFirstOrderedService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pget_first_ordered_service">GetFirstOrderedService</a> function for this routing protocol.

### -field pfnGetNextOrderedService

Pointer to an implementation of the 
<a href="/windows/desktop/api/stm/nc-stm-pget_next_ordered_service">GetNextOrderedService</a> function for this routing protocol.

## -remarks

The members of this structure are pointers to Service Table Management functions implemented in the routing protocol DLL. The routing protocol fills in the address values for these pointers during a call to the 
<a href="/windows/desktop/api/routprot/nc-routprot-pregister_protocol">RegisterProtocol</a> function.

Only routing protocol DLLs that support services need to fill in the 
<b>MPR_SERVICE_CHARACTERISTICS</b> structure.

For a complete description of a particular function pointed to by one of the structure members, see the reference page for that function.

To use this structure, the user should add -DMPR50=1 to the compiler flags.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a>



<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pregister_protocol">RegisterProtocol</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-structures">Routing Protocol Interface Structures</a>
