---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS1_
title: IPSEC_TUNNEL_ENDPOINTS1 (ipsectypes.h)
description: Is used to store end points of a tunnel mode SA.
old-location: fwp\ipsec_tunnel_endpoints1_struct.htm
tech.root: fwp
ms.assetid: 125392f6-fa82-4d86-b8ac-8a481a2da42d
ms.date: 12/05/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS1, IPSEC_TUNNEL_ENDPOINTS1 structure [Filtering], fwp.ipsec_tunnel_endpoints1_struct, ipsectypes/IPSEC_TUNNEL_ENDPOINTS1
ms.topic: struct
f1_keywords:
- ipsectypes/IPSEC_TUNNEL_ENDPOINTS1
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
- IPSEC_TUNNEL_ENDPOINTS1
targetos: Windows
req.typenames: IPSEC_TUNNEL_ENDPOINTS1
req.redist: 
ms.custom: 19H1
---

# IPSEC_TUNNEL_ENDPOINTS1 structure


## -description


The <b>IPSEC_TUNNEL_ENDPOINTS1</b> structure is used to store end points of a tunnel mode SA.
[IPSEC_TUNNEL_ENDPOINTS2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

An [FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a> value that specifies the IP version. In tunnel mode, this is the version of the outer header.


### -field localV4Address

 


### -field localV6Address

 


### -field remoteV4Address

 


### -field remoteV6Address

 


### -field localIfLuid

Optional LUID of the local interface corresponding to the local address specified above.


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




[FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

