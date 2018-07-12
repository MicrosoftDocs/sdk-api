---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS1_
title: IPSEC_TUNNEL_ENDPOINTS1_
author: windows-sdk-content
description: Is used to store end points of a tunnel mode SA.
old-location: fwp\ipsec_tunnel_endpoints1_struct.htm
old-project: fwp
ms.assetid: 125392f6-fa82-4d86-b8ac-8a481a2da42d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS1, IPSEC_TUNNEL_ENDPOINTS1 structure [Filtering], IPSEC_TUNNEL_ENDPOINTS1_, fwp.ipsec_tunnel_endpoints1_struct, ipsectypes/IPSEC_TUNNEL_ENDPOINTS1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: IPSEC_TUNNEL_ENDPOINTS1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_TUNNEL_ENDPOINTS1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_TUNNEL_ENDPOINTS1_ structure


## -description


The <b>IPSEC_TUNNEL_ENDPOINTS1</b> structure is used to store end points of a tunnel mode SA.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_ENDPOINTS1</b> is the specific implementation of IPSEC_TUNNEL_ENDPOINTS used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/a37b13c7-61e4-49be-bd21-db3e7c9bcca5">IPSEC_TUNNEL_ENDPOINTS0</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/091daec1-2c35-4d24-89be-fcdb0354b674">IPSEC_TUNNEL_ENDPOINTS2</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> value that specifies the IP version. In tunnel mode, this is the version of the outer header.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

