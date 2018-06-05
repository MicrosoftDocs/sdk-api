---
UID: NS:fwpstypes.FWPS_ALE_ENDPOINT_PROPERTIES0_
title: FWPS_ALE_ENDPOINT_PROPERTIES0_
author: windows-sdk-content
description: The FWPS_ALE_ENDPOINT_PROPERTIES0 structure specifies the properties of an application layer enforcement (ALE) endpoint.Note  FWPS_ALE_ENDPOINT_PROPERTIES0 is a specific version of FWPS_ALE_ENDPOINT_PROPERTIES.
old-location: netvista\fwps_ale_endpoint_properties0.htm
old-project: netvista
ms.assetid: 1dd5dbd1-b7a7-45a3-8cab-ea62c7eff35b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FWPS_ALE_ENDPOINT_PROPERTIES0, FWPS_ALE_ENDPOINT_PROPERTIES0 structure [Network Drivers Starting with Windows Vista], FWPS_ALE_ENDPOINT_PROPERTIES0_, fwpstypes/FWPS_ALE_ENDPOINT_PROPERTIES0, netvista.fwps_ale_endpoint_properties0, wfp_ref_3_struct_3_fwps_A-E_b528750a-0c8a-4406-81ab-30aa574fb215.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
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
tech.root: 
req.typenames: FWPS_ALE_ENDPOINT_PROPERTIES0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	fwpstypes.h
api_name:
-	FWPS_ALE_ENDPOINT_PROPERTIES0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

