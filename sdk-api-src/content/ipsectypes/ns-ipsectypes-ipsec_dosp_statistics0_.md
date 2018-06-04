---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPSEC_DOSP_STATISTICS0_ structure


## -description


The <b>IPSEC_DOSP_STATISTICS0</b> structure is used to store statistics for IPsec DoS Protection.


## -struct-fields




### -field totalStateEntriesCreated

The total number of state entries that have been created since the computer was last started.


### -field currentStateEntries

The current number of state entries in the table.


### -field totalInboundAllowedIPv6IPsecUnauthPkts

The total number of inbound IPv6 IPsec unauthenticated packets that have been allowed since the computer was last started.


### -field totalInboundRatelimitDiscardedIPv6IPsecUnauthPkts

The total number of inbound IPv6 IPsec unauthenticated packets that have been discarded due to rate limiting since the computer was last started.


### -field totalInboundPerIPRatelimitDiscardedIPv6IPsecUnauthPkts

The total number of inbound IPv6 IPsec unauthenticated packets that have been discarded due to per internal IP address rate limiting since the computer was last started.


### -field totalInboundOtherDiscardedIPv6IPsecUnauthPkts

The total number of inbound IPV6 IPsec unauthenticated packets that have been discarded due to all other reasons since the computer was last started.


### -field totalInboundAllowedIPv6IPsecAuthPkts

The total number of inbound IPv6 IPsec authenticated packets that have been allowed since the computer was last started.


### -field totalInboundRatelimitDiscardedIPv6IPsecAuthPkts

The total number of inbound IPv6 IPsec authenticated packets that have been discarded due to rate limiting since the computer was last started.


### -field totalInboundOtherDiscardedIPv6IPsecAuthPkts

The total number of inbound IPV6 IPsec authenticated packets that have been discarded due to all other reasons since the computer was last started.


### -field totalInboundAllowedICMPv6Pkts

The total number of inbound ICMPv6 packets that have been allowed since the computer was last started.


### -field totalInboundRatelimitDiscardedICMPv6Pkts

The total number of inbound ICMPv6 packets that have been discarded due to rate limiting since the computer was last started.


### -field totalInboundAllowedIPv6FilterExemptPkts

The total number of inbound IPv6 filter exempted packets that have been allowed since the computer was last started.


### -field totalInboundRatelimitDiscardedIPv6FilterExemptPkts

The total number of inbound IPv6 filter exempted packets that have been discarded due to rate limiting since the computer was last started.


### -field totalInboundDiscardedIPv6FilterBlockPkts

The total number of inbound IPv6 filter blocked packets that have been discarded since the computer was last started.


### -field totalInboundAllowedDefBlockExemptPkts

The total number of inbound default-block exempted packets that have been allowed since the computer was last started.


### -field totalInboundRatelimitDiscardedDefBlockExemptPkts

The total number of inbound default-block exempted packets that have been discarded due to rate limiting since the computer was last started.


### -field totalInboundDiscardedDefBlockPkts

The total number of inbound default-block packets that have been discarded since the computer was last started.


### -field currentInboundIPv6IPsecUnauthPerIPRateLimitQueues

The current number of per internal IP address rate limit queues for inbound IPv6 unauthenticated IPsec traffic.


## -remarks



<b>IPSEC_DOSP_STATISTICS0</b> is a specific implementation of IPSEC_DOSP_STATISTICS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

