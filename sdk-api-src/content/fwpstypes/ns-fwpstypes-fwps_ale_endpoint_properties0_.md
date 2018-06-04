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

# FWPS_ALE_ENDPOINT_PROPERTIES0_ structure


## -description


The <b>FWPS_ALE_ENDPOINT_PROPERTIES0</b> structure specifies the properties of an application layer
  enforcement (ALE) endpoint.
<div class="alert"><b>Note</b>  <b>FWPS_ALE_ENDPOINT_PROPERTIES0</b> is a specific version of <b>FWPS_ALE_ENDPOINT_PROPERTIES</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field endpointId

The unique identifier of the endpoint.


### -field ipVersion

The internet protocol version of the endpoint expressed as a value from the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> enumeration.


### -field localV4Address

The local address for IPv4 endpoints.


### -field localV6Address

The local address for IPv6 endpoints.


### -field remoteV4Address

The remote address for IPv4 endpoints.


### -field remoteV6Address

The remote address for IPv6 endpoints.


### -field ipProtocol

The protocol being used by the endpoint.


### -field localPort

The local port number of the endpoint.


### -field remotePort

The remote port number of the endpoint.


### -field localTokenModifiedId

The local token modified identifier.


### -field mmSaId

Use this identifier to correlate this IPsec security assication (SA) with the Internet Key Exchange (IKE) SA that generated it.


### -field qmSaId

SA identifier used by IPsec when choosing the SA to expire. For an IPsec SA
     pair, the qmSaId must be the same between the initiating and responding machines and across inbound and
     outbound SA bundles. For different IPsec pairs, the qmSaId must be different.


### -field ipsecStatus

The IPsec status of the endpoint.


### -field flags

This member is reserved for future use.


### -field appId

The application identifier associated with the endpoint.


## -remarks



Endpoints enumerated by calling 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff551126">FwpsAleEndpointEnum0</a> are defined by
    FWPS_ALE_ENDPOINT_PROPERTIES0 structures.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551126">FwpsAleEndpointEnum0</a>
 

 

