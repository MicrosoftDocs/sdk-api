---
UID: NS:ipsectypes.IPSEC_SA_DETAILS1_
title: IPSEC_SA_DETAILS1 (ipsectypes.h)
description: Is used to store information returned when enumerating IPsec security associations (SAs). (IPSEC_SA_DETAILS1)
helpviewer_keywords: ["IPSEC_SA_DETAILS1","IPSEC_SA_DETAILS1 structure [Filtering]","fwp.ipsec_sa_details1_struct","ipsectypes/IPSEC_SA_DETAILS1"]
old-location: fwp\ipsec_sa_details1_struct.htm
tech.root: fwp
ms.assetid: 257e7ac0-9cb4-45aa-b7e5-107bb3483ab9
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_DETAILS1, IPSEC_SA_DETAILS1 structure [Filtering], fwp.ipsec_sa_details1_struct, ipsectypes/IPSEC_SA_DETAILS1
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: IPSEC_SA_DETAILS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_DETAILS1_
 - ipsectypes/IPSEC_SA_DETAILS1_
 - IPSEC_SA_DETAILS1
 - ipsectypes/IPSEC_SA_DETAILS1
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
 - IPSEC_SA_DETAILS1
---

# IPSEC_SA_DETAILS1 structure


## -description

The <b>IPSEC_SA_DETAILS1</b> structure is used to store information returned when enumerating IPsec security associations (SAs).
[IPSEC_SA_DETAILS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details0) is available.</div><div> </div>

## -struct-fields

### -field ipVersion

An [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) value that specifies the IP version. In tunnel mode, this is the version of the outer header.

### -field saDirection

An [FWP_DIRECTION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction) value that indicates the direction of the IPsec SA.

### -field traffic

An [IPSEC_TRAFFIC1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1) structure that specifies the traffic being secured by this IPsec SA. In tunnel mode, this contains both the tunnel endpoints and Quick Mode (QM)  traffic selectors.

### -field saBundle

An [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure that specifies various parameters of the SA .

### -field udpEncapsulation

An [IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0) structure that stores the UDP 
   encapsulation ports if UDP-ESP encapsulation is enabled on the SA.

Available if <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field transportFilter

An [FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0) structure that specifies the transport layer filter that corresponds to this IPsec SA.

### -field virtualIfTunnelInfo

An [IPSEC_VIRTUAL_IF_TUNNEL_INFO0](/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0) structure that specifies the virtual interface tunnel information. Only supported by Internet Key Exchange version 2 (IKEv2).

## -see-also

[FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)



[FWP_DIRECTION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction)



[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



[IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)



[IPSEC_TRAFFIC1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1)



[IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)



[IPSEC_VIRTUAL_IF_TUNNEL_INFO0](/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
