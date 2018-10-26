---
UID: NS:stm._MPR50_SERVICE_CHARACTERISTICS
title: "_MPR50_SERVICE_CHARACTERISTICS"
author: windows-sdk-content
description: The MPR_SERVICE_CHARACTERISTICS structure contains information used to register a routing protocol with the router manager.
old-location: rras\mpr_service_characteristics.htm
tech.root: rras
ms.assetid: 92a117ae-3a5f-4702-a936-8e23bc575763
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PMPR_SERVICE_CHARACTERISTICS, DEMAND_UPDATE_ROUTES, DEMAND_UPDATE_SERVICES, MPR50_SERVICE_CHARACTERISTICS, MPR_SERVICE_CHARACTERISTICS, MPR_SERVICE_CHARACTERISTICS structure [RAS], PMPR_SERVICE_CHARACTERISTICS, PMPR_SERVICE_CHARACTERISTICS structure pointer [RAS], ROUTING, SERVICES, _MPR50_SERVICE_CHARACTERISTICS, _mpr_mpr_service_characteristics, routprot/MPR_SERVICE_CHARACTERISTICS, routprot/PMPR_SERVICE_CHARACTERISTICS, rras.mpr_service_characteristics, stm/MPR_SERVICE_CHARACTERISTICS, stm/PMPR_SERVICE_CHARACTERISTICS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: MPR50_SERVICE_CHARACTERISTICS
req.redist: 
---

# _MPR50_SERVICE_CHARACTERISTICS structure


## -description


The 
<b>MPR_SERVICE_CHARACTERISTICS</b> structure contains information used to register a routing protocol with the router manager.


## -struct-fields




### -field mscMpr40ServiceChars

 




#### - dwProtocolId

Specifies the routing protocol that the router manager requests the DLL to register. (A common name space is used for all protocol families.)


#### - dwVersion

On input, specifies the version of RRAS currently running. 




On output, the routing protocol should specify the version of RRAS that it requires.

The symbol MS_ROUTER_VERSION in the header file Routprot.h is defined to be the RRAS version for a given implementation.


#### - fSupportedFunctionality

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
 


#### - pfnBlockConvertServicesToStatic

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/60d1ee7b-bba3-4dd1-8faf-520a2e3cfad3">BlockConvertServicesToStatic</a> function for this routing protocol.


#### - pfnBlockDeleteStaticServices

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/eb680a9c-aad8-44b5-8c20-af15c1fd8930">BlockDeleteStaticServices</a> function for this routing protocol.


#### - pfnCloseServiceEnumerationHandle

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/c127f914-b655-4b6a-bb13-daeb5e82e343">CloseServiceEnumerationHandle</a> function for this routing protocol.


#### - pfnCreateServiceEnumerationHandle

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a> function for this routing protocol.


#### - pfnCreateStaticService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/529beae6-ba39-417c-8fa6-7b97fc720352">CreateStaticService</a> function for this routing protocol.


#### - pfnDeleteStaticService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/230ddff5-7fd1-4e4e-b4bb-49c427a3f9c7">DeleteStaticService</a> function for this routing protocol.


#### - pfnEnumerateGetNextService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/45d0ccaa-97d5-4a14-9983-dc0ca268ed4b">EnumerateGetNextService</a> function for this routing protocol.


#### - pfnGetFirstOrderedService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/193ca671-3b1a-493f-a655-a27f6348f5d2">GetFirstOrderedService</a> function for this routing protocol.


#### - pfnGetNextOrderedService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/e25d7086-cfb7-41ea-8f4e-7e4f065830d9">GetNextOrderedService</a> function for this routing protocol.


#### - pfnGetServiceCount

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/44ba90c0-a019-4aca-92e2-1e795cbd335d">GetServiceCount</a> function for this routing protocol.


#### - pfnIsService

Pointer to an implementation of the 
<a href="https://msdn.microsoft.com/f2d8e1f4-ce6c-429c-bb14-26c6c75eab7e">IsService</a> function for this routing protocol.


## -remarks



The members of this structure are pointers to Service Table Management functions implemented in the routing protocol DLL. The routing protocol fills in the address values for these pointers during a call to the 
<a href="https://msdn.microsoft.com/b9027ef9-e573-4df0-b37e-d09956c1f8ee">RegisterProtocol</a> function.

Only routing protocol DLLs that support services need to fill in the 
<b>MPR_SERVICE_CHARACTERISTICS</b> structure.

For a complete description of a particular function pointed to by one of the structure members, see the reference page for that function.

To use this structure, the user should add -DMPR50=1 to the compiler flags.




## -see-also




<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/f67138b8-de5d-4907-a464-672d57864ebf">Protocol Identifiers</a>



<a href="https://msdn.microsoft.com/b9027ef9-e573-4df0-b37e-d09956c1f8ee">RegisterProtocol</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/679c74fa-0049-4556-a942-e51160ceb796">Routing Protocol Interface Structures</a>
 

 

