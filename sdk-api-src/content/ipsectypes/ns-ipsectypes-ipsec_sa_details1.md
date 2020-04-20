---
UID: NS:ipsectypes.IPSEC_SA_DETAILS1_
title: IPSEC_SA_DETAILS1 (ipsectypes.h)
description: Is used to store information returned when enumerating IPsec security associations (SAs).helpviewer_keywords: ["IPSEC_SA_DETAILS1","IPSEC_SA_DETAILS1 structure [Filtering]","fwp.ipsec_sa_details1_struct","ipsectypes/IPSEC_SA_DETAILS1"]
old-location: fwp\ipsec_sa_details1_struct.htm
tech.root: fwp
ms.assetid: 257e7ac0-9cb4-45aa-b7e5-107bb3483ab9
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_DETAILS1, IPSEC_SA_DETAILS1 structure [Filtering], fwp.ipsec_sa_details1_struct, ipsectypes/IPSEC_SA_DETAILS1
f1_keywords:
- ipsectypes/IPSEC_SA_DETAILS1
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ipsectypes.h
api_name:
- IPSEC_SA_DETAILS1
targetos: Windows
req.typenames: IPSEC_SA_DETAILS1
req.redist: 
ms.custom: 19H1
---

# IPSEC_SA_DETAILS1 structure


## -description


The <b>IPSEC_SA_DETAILS1</b> structure is used to store information returned when enumerating IPsec security associations (SAs).
[IPSEC_SA_DETAILS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details0)a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

An [FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a> value that specifies the IP version. In tunnel mode, this is the version of the outer header.


### -field saDirection

An [FWP_DIRECTION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction)a> value that indicates the direction of the IPsec SA.


### -field traffic

An [IPSEC_TRAFFIC1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1)a> structure that specifies the traffic being secured by this IPsec SA. In tunnel mode, this contains both the tunnel endpoints and Quick Mode (QM)  traffic selectors.


### -field saBundle

An [IPSEC_SA_BUNDLE1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)a> structure that specifies various parameters of the SA .


### -field udpEncapsulation

An [IPSEC_V4_UDP_ENCAPSULATION0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)a> structure that stores the UDP 
   encapsulation ports if UDP-ESP encapsulation is enabled on the SA.

Available if <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field transportFilter

An [FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a> structure that specifies the transport layer filter that corresponds to this IPsec SA.


### -field virtualIfTunnelInfo

An [IPSEC_VIRTUAL_IF_TUNNEL_INFO0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)a> structure that specifies the virtual interface tunnel information. Only supported by Internet Key Exchange version 2 (IKEv2).


## -see-also




[FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a>



[FWP_DIRECTION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction)a>



[FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a>



[IPSEC_SA_BUNDLE1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)a>



[IPSEC_TRAFFIC1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1)a>



[IPSEC_V4_UDP_ENCAPSULATION0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)a>



[IPSEC_VIRTUAL_IF_TUNNEL_INFO0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

