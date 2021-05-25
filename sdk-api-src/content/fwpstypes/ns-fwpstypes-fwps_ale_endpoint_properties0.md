---
UID: NS:fwpstypes.FWPS_ALE_ENDPOINT_PROPERTIES0_
title: FWPS_ALE_ENDPOINT_PROPERTIES0 (fwpstypes.h)
description: The FWPS_ALE_ENDPOINT_PROPERTIES0 structure specifies the properties of an application layer enforcement (ALE) endpoint.Note  FWPS_ALE_ENDPOINT_PROPERTIES0 is a specific version of FWPS_ALE_ENDPOINT_PROPERTIES.
helpviewer_keywords: ["FWPS_ALE_ENDPOINT_PROPERTIES0","FWPS_ALE_ENDPOINT_PROPERTIES0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_ALE_ENDPOINT_PROPERTIES0","netvista.fwps_ale_endpoint_properties0","wfp_ref_3_struct_3_fwps_A-E_b528750a-0c8a-4406-81ab-30aa574fb215.xml"]
old-location: netvista\fwps_ale_endpoint_properties0.htm
tech.root: NetVista
ms.assetid: 1dd5dbd1-b7a7-45a3-8cab-ea62c7eff35b
ms.date: 12/05/2018
ms.keywords: FWPS_ALE_ENDPOINT_PROPERTIES0, FWPS_ALE_ENDPOINT_PROPERTIES0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_ALE_ENDPOINT_PROPERTIES0, netvista.fwps_ale_endpoint_properties0, wfp_ref_3_struct_3_fwps_A-E_b528750a-0c8a-4406-81ab-30aa574fb215.xml
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPS_ALE_ENDPOINT_PROPERTIES0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_ALE_ENDPOINT_PROPERTIES0_
 - fwpstypes/FWPS_ALE_ENDPOINT_PROPERTIES0_
 - FWPS_ALE_ENDPOINT_PROPERTIES0
 - fwpstypes/FWPS_ALE_ENDPOINT_PROPERTIES0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_ALE_ENDPOINT_PROPERTIES0
---

# FWPS_ALE_ENDPOINT_PROPERTIES0 structure


## -description

The <b>FWPS_ALE_ENDPOINT_PROPERTIES0</b> structure specifies the properties of an application layer
  enforcement (ALE) endpoint.
<div class="alert"><b>Note</b>  <b>FWPS_ALE_ENDPOINT_PROPERTIES0</b> is a specific version of <b>FWPS_ALE_ENDPOINT_PROPERTIES</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field endpointId

The unique identifier of the endpoint.

### -field ipVersion

The internet protocol version of the endpoint expressed as a value from the 
     <a href="/previous-versions/windows/hardware/drivers/ff552435(v=vs.85)">FWP_IP_VERSION</a> enumeration.

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

Use this identifier to correlate this IPsec security association (SA) with the Internet Key Exchange (IKE) SA that generated it.

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
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointenum0">FwpsAleEndpointEnum0</a> are defined by
    FWPS_ALE_ENDPOINT_PROPERTIES0 structures.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff552435(v=vs.85)">FWP_IP_VERSION</a>



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointenum0">FwpsAleEndpointEnum0</a>