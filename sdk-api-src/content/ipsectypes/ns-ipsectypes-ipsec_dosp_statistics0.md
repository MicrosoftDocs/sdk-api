---
UID: NS:ipsectypes.IPSEC_DOSP_STATISTICS0_
title: IPSEC_DOSP_STATISTICS0 (ipsectypes.h)
description: The IPSEC_DOSP_STATISTICS0 structure.
helpviewer_keywords: ["IPSEC_DOSP_STATISTICS0","IPSEC_DOSP_STATISTICS0 structure [Filtering]","fwp.ipsec_dosp_statistics0","ipsectypes/IPSEC_DOSP_STATISTICS0"]
old-location: fwp\ipsec_dosp_statistics0.htm
tech.root: fwp
ms.assetid: 951b6aa9-ea96-4256-a304-5b753f2a3656
ms.date: 12/05/2018
ms.keywords: IPSEC_DOSP_STATISTICS0, IPSEC_DOSP_STATISTICS0 structure [Filtering], fwp.ipsec_dosp_statistics0, ipsectypes/IPSEC_DOSP_STATISTICS0
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
targetos: Windows
req.typenames: IPSEC_DOSP_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_DOSP_STATISTICS0_
 - ipsectypes/IPSEC_DOSP_STATISTICS0_
 - IPSEC_DOSP_STATISTICS0
 - ipsectypes/IPSEC_DOSP_STATISTICS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_DOSP_STATISTICS0
---

# IPSEC_DOSP_STATISTICS0 structure


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

<b>IPSEC_DOSP_STATISTICS0</b> is a specific implementation of IPSEC_DOSP_STATISTICS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>