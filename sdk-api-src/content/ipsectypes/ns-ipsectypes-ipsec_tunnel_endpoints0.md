---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS0_
title: IPSEC_TUNNEL_ENDPOINTS0 (ipsectypes.h)
author: windows-sdk-content
description: Is used to store end points of a tunnel mode SA.
old-location: fwp\ipsec_tunnel_endpoints0_struct.htm
tech.root: fwp
ms.assetid: a37b13c7-61e4-49be-bd21-db3e7c9bcca5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS0, IPSEC_TUNNEL_ENDPOINTS0 structure [Filtering], fwp.ipsec_tunnel_endpoints0_struct, ipsectypes/IPSEC_TUNNEL_ENDPOINTS0
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_TUNNEL_ENDPOINTS0"
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
 - IPSEC_TUNNEL_ENDPOINTS0
targetos: Windows
req.typenames: IPSEC_TUNNEL_ENDPOINTS0
req.redist: 
ms.custom: 19H1
---

# IPSEC_TUNNEL_ENDPOINTS0 structure


## -description


The <b>IPSEC_TUNNEL_ENDPOINTS0</b> structure is used to store end points of a tunnel mode SA.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_ENDPOINTS0</b> is the specific implementation of IPSEC_TUNNEL_ENDPOINTS used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1_">IPSEC_TUNNEL_ENDPOINTS1</a> is available. For Windows 8, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2_">IPSEC_TUNNEL_ENDPOINTS2</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

IP version of the addresses.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a> for more information.


### -field localV4Address

 


### -field localV6Address

 


### -field remoteV4Address

 


### -field remoteV6Address

 




#### - ( unnamed union )

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the local tunnel end point address.



#### localV4Address

case(FWP_IP_VERSION_V4)



#### localV6Address

case(FWP_IP_VERSION_V6)

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the remote tunnel end point address.



#### remoteV4Address

case(FWP_IP_VERSION_V4)



#### remoteV6Address

case(FWP_IP_VERSION_V6)


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

