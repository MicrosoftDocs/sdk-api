---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS0_
title: IPSEC_TUNNEL_ENDPOINTS0 (ipsectypes.h)
description: Is used to store end points of a tunnel mode SA. (IPSEC_TUNNEL_ENDPOINTS0)
helpviewer_keywords: ["IPSEC_TUNNEL_ENDPOINTS0","IPSEC_TUNNEL_ENDPOINTS0 structure [Filtering]","fwp.ipsec_tunnel_endpoints0_struct","ipsectypes/IPSEC_TUNNEL_ENDPOINTS0"]
old-location: fwp\ipsec_tunnel_endpoints0_struct.htm
tech.root: fwp
ms.assetid: a37b13c7-61e4-49be-bd21-db3e7c9bcca5
ms.date: 12/05/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS0, IPSEC_TUNNEL_ENDPOINTS0 structure [Filtering], fwp.ipsec_tunnel_endpoints0_struct, ipsectypes/IPSEC_TUNNEL_ENDPOINTS0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IPSEC_TUNNEL_ENDPOINTS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TUNNEL_ENDPOINTS0_
 - ipsectypes/IPSEC_TUNNEL_ENDPOINTS0_
 - IPSEC_TUNNEL_ENDPOINTS0
 - ipsectypes/IPSEC_TUNNEL_ENDPOINTS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_TUNNEL_ENDPOINTS0
---

## -description

The <b>IPSEC_TUNNEL_ENDPOINTS0</b> structure is used to store end points of a tunnel mode SA.
[IPSEC_TUNNEL_ENDPOINTS2](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) is available.

## -struct-fields

### -field ipVersion

IP version of the addresses.

See [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) for more information.

### -field localV4Address

case(FWP_IP_VERSION_V4)

### -field localV6Address

case(FWP_IP_VERSION_V6)

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the remote tunnel end point address.

### -field remoteV4Address

case(FWP_IP_VERSION_V4)

### -field remoteV6Address

case(FWP_IP_VERSION_V6)

## -remarks

For the unnamed union containing the local tunnel end point address, switch_type(FWP_IP_VERSION), switch_is(ipVersion).

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API structures</a>
