---
UID: NS:dhcpsapi.DHCPV6_STATELESS_SCOPE_STATS
title: DHCPV6_STATELESS_SCOPE_STATS
author: windows-sdk-content
description: The DHCPV6_STATELESS_SCOPE_STATS structure defines the address counters for a specific IPv6 stateless subnet. The number of stateless IPv6 clients added and removed from the stateless client inventory are stored in this structure.
old-location: dhcp\dhcpv6_stateless_scope_stats.htm
old-project: DHCP
ms.assetid: edb099a6-18eb-49b1-8f97-7f0b32a2430a
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCPV6_STATELESS_SCOPE_STATS, *PDHCPV6_STATELESS_SCOPE_STATS, DHCPV6_STATELESS_SCOPE_STATS, DHCPV6_STATELESS_SCOPE_STATS structure [DHCP], LPDHCPV6_STATELESS_SCOPE_STATS, LPDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP], PDHCPV6_STATELESS_SCOPE_STATS, PDHCPV6_STATELESS_SCOPE_STATS structure pointer [DHCP], dhcp.dhcpv6_stateless_scope_stats, dhcpsapi/DHCPV6_STATELESS_SCOPE_STATS, dhcpsapi/LPDHCPV6_STATELESS_SCOPE_STATS, dhcpsapi/PDHCPV6_STATELESS_SCOPE_STATS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCPV6_STATELESS_SCOPE_STATS, *PDHCPV6_STATELESS_SCOPE_STATS, *LPDHCPV6_STATELESS_SCOPE_STATS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV6_STATELESS_SCOPE_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DHCPV6_STATELESS_SCOPE_STATS structure


## -description


The <b>DHCPV6_STATELESS_SCOPE_STATS</b> structure defines the address counters for a specific IPv6 stateless subnet. The number of stateless IPv6 clients added and removed from the stateless client inventory are stored in this structure.




## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the IPv6 prefix of the DHCPv6 stateless scope.


### -field NumStatelessClientsAdded

Integer that specifies the number of IPv6 stateless clients that have been added to the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.


### -field NumStatelessClientsRemoved

Integer that specifies the number of IPv6 stateless clients that have been removed from the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.


## -see-also




<a href="https://msdn.microsoft.com/8C0E26F3-9496-497C-9E05-9995CC322189">DHCPV6_STATELESS_STATS</a>



<a href="https://msdn.microsoft.com/4f6ba79c-5ab5-4d89-907d-83bdddbd09a2">DhcpV6GetStatelessStatistics</a>
 

 

