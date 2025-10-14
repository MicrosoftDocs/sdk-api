---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS2_
title: IPSEC_TUNNEL_ENDPOINTS2 (ipsectypes.h)
description: Is used to store end points of a tunnel mode SA. (IPSEC_TUNNEL_ENDPOINTS2)
helpviewer_keywords: ["IPSEC_TUNNEL_ENDPOINTS2","IPSEC_TUNNEL_ENDPOINTS2 structure [Filtering]","fwp.ipsec_tunnel_endpoints2","ipsectypes/IPSEC_TUNNEL_ENDPOINTS2"]
old-location: fwp\ipsec_tunnel_endpoints2.htm
tech.root: fwp
ms.assetid: 091daec1-2c35-4d24-89be-fcdb0354b674
ms.date: 12/05/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS2, IPSEC_TUNNEL_ENDPOINTS2 structure [Filtering], fwp.ipsec_tunnel_endpoints2, ipsectypes/IPSEC_TUNNEL_ENDPOINTS2
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_TUNNEL_ENDPOINTS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TUNNEL_ENDPOINTS2_
 - ipsectypes/IPSEC_TUNNEL_ENDPOINTS2_
 - IPSEC_TUNNEL_ENDPOINTS2
 - ipsectypes/IPSEC_TUNNEL_ENDPOINTS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ipsectypes.h
api_name:
 - IPSEC_TUNNEL_ENDPOINTS2
---

## -description

The <b>IPSEC_TUNNEL_ENDPOINTS2</b> structure is used to store end points of a tunnel mode SA.
[IPSEC_TUNNEL_ENDPOINTS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) is available. For Windows Vista, [IPSEC_TUNNEL_ENDPOINTS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) is available.

## -struct-fields

### -field ipVersion

Type: [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)</b>

Specifies the IP version. In tunnel mode, this is the version of the outer header.

### -field localV4Address

Type: <b>UINT32</b>

case(FWP_IP_VERSION_V4)

### -field localV6Address

Type: <b>UINT8[16]</b>

case(FWP_IP_VERSION_V6)

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the remote tunnel end point address.

### -field remoteV4Address

Type: <b>UINT32</b>

case(FWP_IP_VERSION_V4)

### -field remoteV6Address

Type: <b>UINT8[16]</b>

case(FWP_IP_VERSION_V6)

### -field localIfLuid

Type: <b>UINT64</b>

Optional LUID of the local interface corresponding to the local address specified above.

### -field remoteFqdn

Type: <b>wchar_t*</b>

Configuration of multiple remote addresses and fully qualified domain names  for asymmetric tunneling support.

### -field numAddresses

Type: <b>UINT32</b>

The number of remote tunnel addresses.

### -field remoteAddresses

Type: [IPSEC_TUNNEL_ENDPOINT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)*</b>

[size_is(numAddresses)]

The remote tunnel end point address information.

## -remarks

For the unnamed union containing the local tunnel end point address, switch_type(FWP_IP_VERSION), switch_is(ipVersion).

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API structures</a>
