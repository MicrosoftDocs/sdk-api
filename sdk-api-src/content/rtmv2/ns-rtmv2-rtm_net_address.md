---
UID: NS:rtmv2._RTM_NET_ADDRESS
title: RTM_NET_ADDRESS (rtmv2.h)
description: The RTM_NET_ADDRESS structure is used to communicate address information to the routing table manager for any address family. The address family must use only with contiguous address masks that are less than 8 bytes.
helpviewer_keywords: ["*PRTM_NET_ADDRESS","PRTM_NET_ADDRESS","PRTM_NET_ADDRESS structure pointer [RAS]","RTM_NET_ADDRESS","RTM_NET_ADDRESS structure [RAS]","_rtmv2ref_rtm_net_address","rras.rtm_net_address","rtmv2/PRTM_NET_ADDRESS","rtmv2/RTM_NET_ADDRESS"]
old-location: rras\rtm_net_address.htm
tech.root: RRAS
ms.assetid: 92c4e797-9b73-438d-b4df-9739fae9d5c8
ms.date: 12/05/2018
ms.keywords: '*PRTM_NET_ADDRESS, PRTM_NET_ADDRESS, PRTM_NET_ADDRESS structure pointer [RAS], RTM_NET_ADDRESS, RTM_NET_ADDRESS structure [RAS], _rtmv2ref_rtm_net_address, rras.rtm_net_address, rtmv2/PRTM_NET_ADDRESS, rtmv2/RTM_NET_ADDRESS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTM_NET_ADDRESS, *PRTM_NET_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_NET_ADDRESS
 - rtmv2/_RTM_NET_ADDRESS
 - PRTM_NET_ADDRESS
 - rtmv2/PRTM_NET_ADDRESS
 - RTM_NET_ADDRESS
 - rtmv2/RTM_NET_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_NET_ADDRESS
---

# RTM_NET_ADDRESS structure


## -description

The <a href="/windows/win32/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure is used to communicate address information to the routing table manager for any address family. The address family must use only with contiguous address masks that are less than 8 bytes.

## -struct-fields

### -field AddressFamily

Specifies the type of network address for this address (such as IPv4).

### -field NumBits

Specifies the number of bits in the network part of the <b>AddrBits</b> bit array (for example, 192.168.0.0 has 8 bits).

### -field AddrBits

Specifies an array of bits that form the address prefix.

## -remarks

If the client specifies an address and a mask length that do not correspond to each other, inconsistent results are returned by the routing table manager. For example, if a client specifies an address as 10.10.10.10 and a length as 24 when calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_len">RTM_IPV4_SET_ADDR_AND_LEN</a>, the routing table manager may return an incorrect <i>NetAddress</i>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatedestenum">RtmCreateDestEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatenexthopenum">RtmCreateNextHopEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreaterouteenum">RtmCreateRouteEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchroute">RtmGetExactMatchRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetrouteinfo">RtmGetRouteInfo</a>