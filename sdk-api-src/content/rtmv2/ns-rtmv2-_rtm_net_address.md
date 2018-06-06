---
UID: NS:rtmv2._RTM_NET_ADDRESS
title: "_RTM_NET_ADDRESS"
author: windows-sdk-content
description: The RTM_NET_ADDRESS structure is used to communicate address information to the routing table manager for any address family. The address family must use only with contiguous address masks that are less than 8 bytes.
old-location: rras\rtm_net_address.htm
old-project: RRAS
ms.assetid: 92c4e797-9b73-438d-b4df-9739fae9d5c8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PRTM_NET_ADDRESS, PRTM_NET_ADDRESS, PRTM_NET_ADDRESS structure pointer [RAS], RTM_NET_ADDRESS, RTM_NET_ADDRESS structure [RAS], _RTM_NET_ADDRESS, _rtmv2ref_rtm_net_address, rras.rtm_net_address, rtmv2/PRTM_NET_ADDRESS, rtmv2/RTM_NET_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RTM_NET_ADDRESS, *PRTM_NET_ADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_NET_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RTM_NET_ADDRESS structure


## -description


The 
<a href="https://docs.microsoft.com/">RTM_NET_ADDRESS</a> structure is used to communicate address information to the routing table manager for any address family. The address family must use only with contiguous address masks that are less than 8 bytes.


## -struct-fields




### -field AddressFamily

Specifies the type of network address for this address (such as IPv4).


### -field NumBits

Specifies the number of bits in the network part of the <b>AddrBits</b> bit array (for example, 192.168.0.0 has 8 bits).


### -field AddrBits

Specifies an array of bits that form the address prefix.


## -remarks



If the client specifies an address and a mask length that do not correspond to each other, inconsistent results are returned by the routing table manager. For example, if a client specifies an address as 10.10.10.10 and a length as 24 when calling 
<a href="https://msdn.microsoft.com/c6f60346-51ff-4e1e-9edb-b326184f79cf">RTM_IPV4_SET_ADDR_AND_LEN</a>, the routing table manager may return an incorrect <i>NetAddress</i>.




## -see-also




<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>



<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/6efea7b4-dd44-4b08-999d-62e7f660ed64">RtmCreateDestEnum</a>



<a href="https://msdn.microsoft.com/d26ce475-ea05-4e84-92da-06df9c386858">RtmCreateNextHopEnum</a>



<a href="https://msdn.microsoft.com/9d9c35e8-a9d4-4b30-a92c-f3188e11e317">RtmCreateRouteEnum</a>



<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a>



<a href="https://msdn.microsoft.com/5fc9cde7-9912-409f-85ee-c775b4d6ddc0">RtmGetExactMatchRoute</a>



<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a>



<a href="https://msdn.microsoft.com/13fc70de-f6cd-4e7a-b79d-c2fe811e08a4">RtmGetRouteInfo</a>
 

 

