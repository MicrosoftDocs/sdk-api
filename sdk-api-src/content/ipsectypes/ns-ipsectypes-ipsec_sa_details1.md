---
UID: NS:ipsectypes.IPSEC_SA_DETAILS1_
title: IPSEC_SA_DETAILS1 (ipsectypes.h)

description: Is used to store information returned when enumerating IPsec security associations (SAs).
old-location: fwp\ipsec_sa_details1_struct.htm
tech.root: fwp
ms.assetid: 257e7ac0-9cb4-45aa-b7e5-107bb3483ab9

ms.date: 12/05/2018
ms.keywords: IPSEC_SA_DETAILS1, IPSEC_SA_DETAILS1 structure [Filtering], fwp.ipsec_sa_details1_struct, ipsectypes/IPSEC_SA_DETAILS1
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_SA_DETAILS1"
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
<div class="alert"><b>Note</b>  <b>IPSEC_SA_DETAILS1</b> is the specific implementation of IPSEC_SA_DETAILS used in Windows 7 and later. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details0_">IPSEC_SA_DETAILS0</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

An <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a> value that specifies the IP version. In tunnel mode, this is the version of the outer header.


### -field saDirection

An <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction_">FWP_DIRECTION</a> value that indicates the direction of the IPsec SA.


### -field traffic

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1_">IPSEC_TRAFFIC1</a> structure that specifies the traffic being secured by this IPsec SA. In tunnel mode, this contains both the tunnel endpoints and Quick Mode (QM)  traffic selectors.


### -field saBundle

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1_">IPSEC_SA_BUNDLE1</a> structure that specifies various parameters of the SA .


### -field udpEncapsulation

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0_">IPSEC_V4_UDP_ENCAPSULATION0</a> structure that stores the UDP 
   encapsulation ports if UDP-ESP encapsulation is enabled on the SA.

Available if <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field transportFilter

An <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0_">FWPM_FILTER0</a> structure that specifies the transport layer filter that corresponds to this IPsec SA.


### -field virtualIfTunnelInfo

An <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0_">IPSEC_VIRTUAL_IF_TUNNEL_INFO0</a> structure that specifies the virtual interface tunnel information. Only supported by Internet Key Exchange version 2 (IKEv2).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0_">FWPM_FILTER0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction_">FWP_DIRECTION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1_">IPSEC_SA_BUNDLE1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1_">IPSEC_TRAFFIC1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0_">IPSEC_V4_UDP_ENCAPSULATION0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0_">IPSEC_VIRTUAL_IF_TUNNEL_INFO0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

