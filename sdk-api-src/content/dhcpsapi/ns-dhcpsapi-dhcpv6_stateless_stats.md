---
UID: NS:dhcpsapi.DHCPV6_STATELESS_STATS
title: DHCPV6_STATELESS_STATS (dhcpsapi.h)
description: The DHCPV6_STATELESS_STATS structure defines an array of stateless IPv6 subnet statistics.
helpviewer_keywords: ["*LPDHCPV6_STATELESS_STATS","*PDHCPV6_STATELESS_STATS","DHCPV6_STATELESS_STATS","DHCPV6_STATELESS_STATS structure [DHCP]","LPDHCPV6_STATELESS_STATS","LPDHCPV6_STATELESS_STATS structure pointer [DHCP]","PDHCPV6_STATELESS_STATS","PDHCPV6_STATELESS_STATS structure pointer [DHCP]","dhcp.dhcpv6_stateless_stats","dhcpsapi/DHCPV6_STATELESS_STATS","dhcpsapi/LPDHCPV6_STATELESS_STATS","dhcpsapi/PDHCPV6_STATELESS_STATS"]
old-location: dhcp\dhcpv6_stateless_stats.htm
tech.root: DHCP
ms.assetid: 8C0E26F3-9496-497C-9E05-9995CC322189
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6_STATELESS_STATS, *PDHCPV6_STATELESS_STATS, DHCPV6_STATELESS_STATS, DHCPV6_STATELESS_STATS structure [DHCP], LPDHCPV6_STATELESS_STATS, LPDHCPV6_STATELESS_STATS structure pointer [DHCP], PDHCPV6_STATELESS_STATS, PDHCPV6_STATELESS_STATS structure pointer [DHCP], dhcp.dhcpv6_stateless_stats, dhcpsapi/DHCPV6_STATELESS_STATS, dhcpsapi/LPDHCPV6_STATELESS_STATS, dhcpsapi/PDHCPV6_STATELESS_STATS'
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
req.typenames: DHCPV6_STATELESS_STATS, *PDHCPV6_STATELESS_STATS, *LPDHCPV6_STATELESS_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDHCPV6_STATELESS_STATS
 - dhcpsapi/PDHCPV6_STATELESS_STATS
 - DHCPV6_STATELESS_STATS
 - dhcpsapi/DHCPV6_STATELESS_STATS
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
 - DHCPV6_STATELESS_STATS
---

# DHCPV6_STATELESS_STATS structure


## -description

The <b>DHCPV6_STATELESS_STATS</b> structure defines an array of stateless IPv6 subnet statistics.

## -struct-fields

### -field NumScopes

Integer that specifies the number of subnet statistics in <i>ScopeStats</i>.

### -field ScopeStats

Pointer to a list of <a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_scope_stats">DHCPV6_STATELESS_SCOPE_STATS</a> structures.

### -field size_is

### -field size_is.NumScopes

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_scope_stats">DHCPV6_STATELESS_SCOPE_STATS</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6getstatelessstatistics">DhcpV6GetStatelessStatistics</a>

