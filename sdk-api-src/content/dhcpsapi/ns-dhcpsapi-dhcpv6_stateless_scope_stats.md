---
UID: NS:dhcpsapi.DHCPV6_STATELESS_SCOPE_STATS
title: DHCPV6_STATELESS_SCOPE_STATS (dhcpsapi.h)
description: The DHCPV6_STATELESS_SCOPE_STATS structure defines the address counters for a specific IPv6 stateless subnet. The number of stateless IPv6 clients added and removed from the stateless client inventory are stored in this structure.
helpviewer_keywords: ["*LPDHCPV6_STATELESS_SCOPE_STATS","*PDHCPV6_STATELESS_SCOPE_STATS","DHCPV6_STATELESS_SCOPE_STATS","DHCPV6_STATELESS_SCOPE_STATS structure [DHCP]","LPDHCPV6_STATELESS_SCOPE_STATS","LPDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP]","PDHCPV6_STATELESS_SCOPE_STATS","PDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP]","dhcp.dhcpv6_stateless_scope_stats","dhcpsapi/DHCPV6_STATELESS_SCOPE_STATS","dhcpsapi/LPDHCPV6_STATELESS_SCOPE_STATS","dhcpsapi/PDHCPV6_STATELESS_SCOPE_STATS"]
old-location: dhcp\dhcpv6_stateless_scope_stats.htm
tech.root: DHCP
ms.assetid: edb099a6-18eb-49b1-8f97-7f0b32a2430a
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6_STATELESS_SCOPE_STATS, *PDHCPV6_STATELESS_SCOPE_STATS, DHCPV6_STATELESS_SCOPE_STATS, DHCPV6_STATELESS_SCOPE_STATS structure [DHCP], LPDHCPV6_STATELESS_SCOPE_STATS, LPDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP], PDHCPV6_STATELESS_SCOPE_STATS, PDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP], dhcp.dhcpv6_stateless_scope_stats, dhcpsapi/DHCPV6_STATELESS_SCOPE_STATS, dhcpsapi/LPDHCPV6_STATELESS_SCOPE_STATS, dhcpsapi/PDHCPV6_STATELESS_SCOPE_STATS'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCPV6_STATELESS_SCOPE_STATS, *PDHCPV6_STATELESS_SCOPE_STATS, *LPDHCPV6_STATELESS_SCOPE_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDHCPV6_STATELESS_SCOPE_STATS
 - dhcpsapi/PDHCPV6_STATELESS_SCOPE_STATS
 - DHCPV6_STATELESS_SCOPE_STATS
 - dhcpsapi/DHCPV6_STATELESS_SCOPE_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV6_STATELESS_SCOPE_STATS
---

# DHCPV6_STATELESS_SCOPE_STATS structure


## -description

The <b>DHCPV6_STATELESS_SCOPE_STATS</b> structure defines the address counters for a specific IPv6 stateless subnet. The number of stateless IPv6 clients added and removed from the stateless client inventory are stored in this structure.

## -struct-fields

### -field SubnetAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that specifies the IPv6 prefix of the DHCPv6 stateless scope.

### -field NumStatelessClientsAdded

Integer that specifies the number of IPv6 stateless clients that have been added to the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.

### -field NumStatelessClientsRemoved

Integer that specifies the number of IPv6 stateless clients that have been removed from the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_stats">DHCPV6_STATELESS_STATS</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6getstatelessstatistics">DhcpV6GetStatelessStatistics</a>

