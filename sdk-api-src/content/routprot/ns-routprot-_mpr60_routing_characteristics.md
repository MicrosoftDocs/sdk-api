---
UID: NS:routprot._MPR60_ROUTING_CHARACTERISTICS
title: "_MPR60_ROUTING_CHARACTERISTICS"
author: windows-sdk-content
description: The MPR_ROUTING_CHARACTERISTICS structure contains information used to register routing protocols with the router manager.
old-location: rras\mpr_routing_characteristics.htm
old-project: rras
ms.assetid: 7046c4c2-b0bd-4459-b361-e46ce876823f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMPR_ROUTING_CHARACTERISTICS, DEMAND_UPDATE_ROUTES, DEMAND_UPDATE_SERVICES, MPR50_ROUTING_CHARACTERISTICS, MPR50_ROUTING_CHARACTERISTICS structure [RAS], MPR60_ROUTING_CHARACTERISTICS, MPR_ROUTING_CHARACTERISTICS, MPR_ROUTING_CHARACTERISTICS structure [RAS], PMPR_ROUTING_CHARACTERISTICS, PMPR_ROUTING_CHARACTERISTICS structure pointer [RAS], ROUTING, SERVICES, _MPR60_ROUTING_CHARACTERISTICS, _mpr_mpr_routing_characteristics, routprot/MPR_ROUTING_CHARACTERISTICS, routprot/PMPR_ROUTING_CHARACTERISTICS, rras.mpr_routing_characteristics"
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
req.typenames: MPR60_ROUTING_CHARACTERISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - MPR50_ROUTING_CHARACTERISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _MPR60_ROUTING_CHARACTERISTICS structure


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
<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a> function for this routing protocol.


### -field pfnStartComplete

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/1dace3a7-8e97-405c-b1fe-f5a67c05fb0c">StartComplete</a> function for this routing protocol.


### -field pfnStopProtocol

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/8b9459f8-152c-4ec1-9ed0-2b27a56f521d">StopProtocol</a> function for this routing protocol.


### -field pfnGetGlobalInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/89d4ca42-8f78-40bd-96f0-ad10181cb2d4">GetGlobalInfo</a> function for this routing protocol.


### -field pfnSetGlobalInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/fd977a71-bfa7-40e4-9afc-4824989f857f">SetGlobalInfo</a> function for this routing protocol.


### -field pfnQueryPower

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/591082fb-ef1e-4271-bf6c-d5034bdbae99">QueryPower</a> function for this routing protocol.


### -field pfnSetPower

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/595e1743-04eb-4490-8548-1ce5ce00e144">SetPower</a> function for this routing protocol.


### -field pfnAddInterface

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/d2a90d20-7a1f-4301-adab-76224a4f8310">AddInterface</a> function for this routing protocol.


### -field pfnDeleteInterface

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/0b4c24d4-2588-412e-b3ec-dd73cbdac921">DeleteInterface</a> function for this routing protocol.


### -field pfnInterfaceStatus

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/8fd674a6-375e-450c-bd6b-4f252977dd8e">InterfaceStatus</a> function for this routing protocol.


### -field pfnGetInterfaceInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/ec662772-f864-4108-b676-3fa501b3b927">GetInterfaceInfo</a> function for this routing protocol.


### -field pfnSetInterfaceInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/abcfa220-a860-48cc-92c5-60ce655678b7">SetInterfaceInfo</a> function for this routing protocol.


### -field pfnGetEventMessage

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/59aa7bd8-3510-4ca0-90f1-2667dcb4abf0">GetEventMessage</a> function for this routing protocol.


### -field pfnUpdateRoutes

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/5942c856-f504-4e2d-86c8-f3207c787ed5">DoUpdateRoutes</a> function for this routing protocol.


### -field pfnConnectClient

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/548d8411-ca03-4316-9adb-3b4b48a740d9">ConnectClient</a> function for this routing protocol.


### -field pfnDisconnectClient

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/45859605-2981-4236-9546-9b88e07673fe">DisconnectClient</a> function for this routing protocol.


### -field pfnGetNeighbors

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/31a28a43-3cfd-4d3c-813e-8f8289d99712">GetNeighbors</a> function for this routing protocol.


### -field pfnGetMfeStatus

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/518eb335-13b9-4980-90fc-11cdd7ef8f1a">GetMfeStatus</a> function for this routing protocol.


### -field pfnMibCreateEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/b3e8eca6-6d8d-4385-8c94-7269878810c0">MibCreate</a> function for this routing protocol.


### -field pfnMibDeleteEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/3097843e-ffa6-443a-9ee8-1034f3ed474a">MibDelete</a> function for this routing protocol.


### -field pfnMibGetEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/a6f3d450-0ca1-4c22-9e48-addf317cac2a">MibGet</a> function for this routing protocol.


### -field pfnMibSetEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/f1df3476-f6c5-4f7e-bc86-83e5f8d0cd57">MibSet</a> function for this routing protocol.


### -field pfnMibGetFirstEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/3aef09e2-6314-4de8-a9dd-e02c13e0145c">MibGetFirst</a> function for this routing protocol.


### -field pfnMibGetNextEntry

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/00047426-11b6-4b68-8a44-45608611eafe">MibGetNext</a> function for this routing protocol.


### -field pfnMibSetTrapInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/28056113-82a5-4493-ba49-509db3606fa0">MibSetTrapInfo</a> function for this routing protocol.


### -field pfnMibGetTrapInfo

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/2eb77b83-27bb-414b-8fbf-519d5e0cb08a">MibGetTrapInfo</a> function for this routing protocol.


### -field pfnProtocolAction

 


### -field pfnGetStatistics

 


### -field pfnGetRoutingDomainGlobalInfo

 


### -field pfnSetRoutingDomainGlobalInfo

 


### -field pfnBufferFree

 




## -remarks



Most of the members of this structure are pointers to functions implemented in the routing protocol DLL. The routing protocol fills in the address values for these pointers during a call to the 
<a href="https://msdn.microsoft.com/b9027ef9-e573-4df0-b37e-d09956c1f8ee">RegisterProtocol</a> function.

For a complete description of a particular function pointed to by one of the structure members, see the reference page for that function.




## -see-also




<a href="https://msdn.microsoft.com/f67138b8-de5d-4907-a464-672d57864ebf">Protocol Identifiers</a>



<a href="https://msdn.microsoft.com/b9027ef9-e573-4df0-b37e-d09956c1f8ee">RegisterProtocol</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/679c74fa-0049-4556-a942-e51160ceb796">Routing Protocol Interface Structures</a>
 

 

