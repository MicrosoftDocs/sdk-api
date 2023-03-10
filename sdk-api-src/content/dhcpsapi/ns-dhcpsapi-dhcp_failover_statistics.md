---
UID: NS:dhcpsapi._DHCP_FAILOVER_STATISTICS
title: DHCP_FAILOVER_STATISTICS (dhcpsapi.h)
description: The DHCP_FAILOVER_STATISTICS structure defines DHCP server scope statistics that are part of a failover relationship.
helpviewer_keywords: ["*LPDHCP_FAILOVER_STATISTICS","DHCP_FAILOVER_STATISTICS","DHCP_FAILOVER_STATISTICS structure [DHCP]","LPDHCP_FAILOVER_STATISTICS","LPDHCP_FAILOVER_STATISTICS structure pointer [DHCP]","dhcp.dhcp_failover_statistics","dhcpsapi/DHCP_FAILOVER_STATISTICS","dhcpsapi/LPDHCP_FAILOVER_STATISTICS"]
old-location: dhcp\dhcp_failover_statistics.htm
tech.root: DHCP
ms.assetid: a06d873c-fc82-40c1-be3e-45f24328897d
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_STATISTICS, DHCP_FAILOVER_STATISTICS, DHCP_FAILOVER_STATISTICS structure [DHCP], LPDHCP_FAILOVER_STATISTICS, LPDHCP_FAILOVER_STATISTICS structure pointer [DHCP], dhcp.dhcp_failover_statistics, dhcpsapi/DHCP_FAILOVER_STATISTICS, dhcpsapi/LPDHCP_FAILOVER_STATISTICS'
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
req.typenames: DHCP_FAILOVER_STATISTICS, *LPDHCP_FAILOVER_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FAILOVER_STATISTICS
 - dhcpsapi/_DHCP_FAILOVER_STATISTICS
 - LPDHCP_FAILOVER_STATISTICS
 - dhcpsapi/LPDHCP_FAILOVER_STATISTICS
 - DHCP_FAILOVER_STATISTICS
 - dhcpsapi/DHCP_FAILOVER_STATISTICS
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
 - DHCP_FAILOVER_STATISTICS
---

## -description

The <b>DHCP_FAILOVER_STATISTICS</b> structure defines DHCP server scope statistics that are part of a failover relationship.

## -struct-fields

### -field NumAddr

Value that specifies the total number of addresses in a DHCPv4 scope that are part of a failover relationship.

### -field AddrFree

Value that specifies the total number of free IPv4 addresses that can be leased out to clients in a DHCPv4 scope that are part of a failover relationship.

### -field AddrInUse

Value that specifies the total number of IPv4 addresses that are leased out to clients in a DHCPv4 scope that are part of a failover relationship.

### -field PartnerAddrFree

Value that specifies the number of free IPv4 addresses on the partner server that can be leased out to clients in a DHCPv4 scope that are part of a failover relationship.

### -field ThisAddrFree

Value that specifies the number of free IPv4 addresses on the local server that can be leased out to clients in a DHCPv4 scope that are part of a failover relationship.

### -field PartnerAddrInUse

Value that specifies the number of IPv4 addresses on the partner server that are leased out to clients in a DHCPv4 scope that are part of a failover relationship.

### -field ThisAddrInUse

Value that specifies the number of IPv4 addresses on the local server that are leased out to clients in a DHCPv4 scope that are part of a failover relationship.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscopestatistics">DhcpV4FailoverGetScopeStatistics</a>
