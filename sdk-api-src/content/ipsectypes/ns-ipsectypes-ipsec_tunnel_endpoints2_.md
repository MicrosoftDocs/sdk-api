---
UID: NS:ipsectypes.IPSEC_TUNNEL_ENDPOINTS2_
title: IPSEC_TUNNEL_ENDPOINTS2_
author: windows-sdk-content
description: Is used to store end points of a tunnel mode SA.
old-location: fwp\ipsec_tunnel_endpoints2.htm
tech.root: fwp
ms.assetid: 091daec1-2c35-4d24-89be-fcdb0354b674
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPSEC_TUNNEL_ENDPOINTS2, IPSEC_TUNNEL_ENDPOINTS2 structure [Filtering], IPSEC_TUNNEL_ENDPOINTS2_, fwp.ipsec_tunnel_endpoints2, ipsectypes/IPSEC_TUNNEL_ENDPOINTS2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ipsectypes.h
api_name:
 - IPSEC_TUNNEL_ENDPOINTS2
product: Windows
targetos: Windows
req.typenames: IPSEC_TUNNEL_ENDPOINTS2
req.redist: 
---

# IPSEC_TUNNEL_ENDPOINTS2_ structure


## -description


The <b>IPSEC_TUNNEL_ENDPOINTS2</b> structure is used to store end points of a tunnel mode SA.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_ENDPOINTS2</b> is the specific implementation of IPSEC_TUNNEL_ENDPOINTS used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/125392f6-fa82-4d86-b8ac-8a481a2da42d">IPSEC_TUNNEL_ENDPOINTS1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/a37b13c7-61e4-49be-bd21-db3e7c9bcca5">IPSEC_TUNNEL_ENDPOINTS0</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

Type: <b><a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a></b>

Specifies the IP version. In tunnel mode, this is the version of the outer header.


### -field localV4Address

 


### -field localV6Address

 


### -field remoteV4Address

 


### -field remoteV6Address

 


### -field localIfLuid

Type: <b>UINT64</b>

Optional LUID of the local interface corresponding to the local address specified above.


### -field remoteFqdn

Type: <b>wchar_t*</b>

Configuration of multiple remote addresses and fully qualified domain names  for asymmetric tunneling support.


### -field numAddresses

Type: <b>UINT32</b>

The number of remote tunnel addresses.


### -field remoteAddresses

Type: <b><a href="https://msdn.microsoft.com/e536e9b0-1128-4548-9461-3cdeba509873">IPSEC_TUNNEL_ENDPOINT0</a>*</b>

 [size_is(numAddresses)]

The remote tunnel end point address information.


#### - ( unnamed union )

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the local tunnel end point address.



#### localV4Address

<b>Type: <b>UINT32</b>
</b>
case(FWP_IP_VERSION_V4)



#### localV6Address

<b>Type: <b>UINT8[16]</b>
</b>
case(FWP_IP_VERSION_V6)

switch_type(FWP_IP_VERSION), switch_is(ipVersion)

Tagged union containing the remote tunnel end point address.



#### remoteV4Address

<b>Type: <b>UINT32</b>
</b>
case(FWP_IP_VERSION_V4)



#### remoteV6Address

<b>Type: <b>UINT8[16]</b>
</b>
case(FWP_IP_VERSION_V6)


## -see-also




<a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

