---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS0_
title: IPSEC_TUNNEL_ENDPOINTS0_
author: windows-driver-content
description: Is used to store end points of a tunnel mode SA.
old-location: fwp\ipsec_tunnel_endpoints0_struct.htm
old-project: FWP
ms.assetid: a37b13c7-61e4-49be-bd21-db3e7c9bcca5
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS0, IPSEC_TUNNEL_ENDPOINTS0 structure [Filtering], IPSEC_TUNNEL_ENDPOINTS0_, fwp.ipsec_tunnel_endpoints0_struct, ipsectypes/IPSEC_TUNNEL_ENDPOINTS0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: IPSEC_TUNNEL_ENDPOINTS0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_TUNNEL_ENDPOINTS0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_TUNNEL_ENDPOINTS0_ structure


## -description


The <b>IPSEC_TUNNEL_ENDPOINTS0</b> structure is used to store end points of a tunnel mode SA.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_ENDPOINTS0</b> is the specific implementation of IPSEC_TUNNEL_ENDPOINTS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/125392f6-fa82-4d86-b8ac-8a481a2da42d">IPSEC_TUNNEL_ENDPOINTS1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/091daec1-2c35-4d24-89be-fcdb0354b674">IPSEC_TUNNEL_ENDPOINTS2</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

IP version of the addresses.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> for more information.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

