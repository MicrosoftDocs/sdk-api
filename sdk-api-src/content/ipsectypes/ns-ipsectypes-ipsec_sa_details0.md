---
UID: NS:ipsectypes.IPSEC_SA_DETAILS0_
title: IPSEC_SA_DETAILS0 (ipsectypes.h)
description: Is used to store information returned when enumerating IPsec security associations (SAs).helpviewer_keywords: ["IPSEC_SA_DETAILS0","IPSEC_SA_DETAILS0 structure [Filtering]","fwp.ipsec_sa_details0_struct","ipsectypes/IPSEC_SA_DETAILS0"]
old-location: fwp\ipsec_sa_details0_struct.htm
tech.root: fwp
ms.assetid: 261cea6e-4a56-404f-9e5d-70ce95122f9f
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_DETAILS0, IPSEC_SA_DETAILS0 structure [Filtering], fwp.ipsec_sa_details0_struct, ipsectypes/IPSEC_SA_DETAILS0
f1_keywords:
- ipsectypes/IPSEC_SA_DETAILS0
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ipsectypes.h
api_name:
- IPSEC_SA_DETAILS0
targetos: Windows
req.typenames: IPSEC_SA_DETAILS0
req.redist: 
ms.custom: 19H1
---

# IPSEC_SA_DETAILS0 structure


## -description


The <b>IPSEC_SA_DETAILS0</b> structure is used to store information returned when enumerating IPsec security associations (SAs).
[IPSEC_SA_DETAILS1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1)a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

Internet Protocol (IP) version as specified by [FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a>. 


### -field saDirection

Indicates direction of the IPsec SA as specified by [FWP_DIRECTION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction)a>.


### -field traffic

The traffic being secured by this IPsec SA as specified by [IPSEC_TRAFFIC0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic0)a>. 


### -field saBundle

Various parameters of the SA as specified by [IPSEC_SA_BUNDLE0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)a>.


### -field udpEncapsulation

An [IPSEC_V4_UDP_ENCAPSULATION0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)a> structure that stores the UDP 
   encapsulation ports if UDP-ESP encapsulation is enabled on the SA.

Available if <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field transportFilter

The transport layer filter corresponding to this IPsec SA as specified by [FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

