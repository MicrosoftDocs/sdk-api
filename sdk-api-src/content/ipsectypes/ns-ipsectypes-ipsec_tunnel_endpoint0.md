---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINT0_
title: IPSEC_TUNNEL_ENDPOINT0 (ipsectypes.h)
description: Used to store address information for an end point of a tunnel mode SA.
helpviewer_keywords: ["IPSEC_TUNNEL_ENDPOINT0","IPSEC_TUNNEL_ENDPOINT0 structure [Filtering]","fwp.ipsec_tunnel_endpoint0","ipsectypes/IPSEC_TUNNEL_ENDPOINT0"]
old-location: fwp\ipsec_tunnel_endpoint0.htm
tech.root: fwp
ms.assetid: e536e9b0-1128-4548-9461-3cdeba509873
ms.date: 12/05/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINT0, IPSEC_TUNNEL_ENDPOINT0 structure [Filtering], fwp.ipsec_tunnel_endpoint0, ipsectypes/IPSEC_TUNNEL_ENDPOINT0
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
req.typenames: IPSEC_TUNNEL_ENDPOINT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TUNNEL_ENDPOINT0_
 - ipsectypes/IPSEC_TUNNEL_ENDPOINT0_
 - IPSEC_TUNNEL_ENDPOINT0
 - ipsectypes/IPSEC_TUNNEL_ENDPOINT0
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
 - IPSEC_TUNNEL_ENDPOINT0
---

## -description

The <b>IPSEC_TUNNEL_ENDPOINT0</b> structure is used to store address information for an end point of a tunnel mode SA.

## -struct-fields

### -field ipVersion

Type: [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)</b>

Specifies the IP version. In tunnel mode, this is the version of the outer header.

### -field v4Address

Type: <b>UINT32</b>

case(FWP_IP_VERSION_V4)

### -field v6Address

Type: <b>UINT8[16]</b>

case(FWP_IP_VERSION_V6)

## -remarks

For the unnamed union containing the tunnel end point address, switch_type(FWP_IP_VERSION), switch_is(ipVersion).

<b>IPSEC_TUNNEL_ENDPOINT0</b> is a specific implementation of IPSEC_TUNNEL_ENDPOINT. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)

[IPSEC_TUNNEL_ENDPOINTS2](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API structures</a>
