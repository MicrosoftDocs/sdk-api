---
UID: NS:dhcpsapi.DHCPV6_STATELESS_STATS
title: DHCPV6_STATELESS_STATS
author: windows-sdk-content
description: The DHCPV6_STATELESS_STATS structure defines an array of stateless IPv6 subnet statistics.
old-location: dhcp\dhcpv6_stateless_stats.htm
tech.root: DHCP
ms.assetid: 8C0E26F3-9496-497C-9E05-9995CC322189
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCPV6_STATELESS_STATS, *PDHCPV6_STATELESS_STATS, DHCPV6_STATELESS_STATS, DHCPV6_STATELESS_STATS structure [DHCP], LPDHCPV6_STATELESS_STATS, LPDHCPV6_STATELESS_STATS structure pointer [DHCP], PDHCPV6_STATELESS_STATS, PDHCPV6_STATELESS_STATS structure pointer [DHCP], dhcp.dhcpv6_stateless_stats, dhcpsapi/DHCPV6_STATELESS_STATS, dhcpsapi/LPDHCPV6_STATELESS_STATS, dhcpsapi/PDHCPV6_STATELESS_STATS"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV6_STATELESS_STATS
product: Windows
targetos: Windows
req.typenames: DHCPV6_STATELESS_STATS, *PDHCPV6_STATELESS_STATS, *LPDHCPV6_STATELESS_STATS
req.redist: 
---

# DHCPV6_STATELESS_STATS structure


## -description


The <b>DHCPV6_STATELESS_STATS</b> structure defines an array of stateless IPv6 subnet statistics.


## -struct-fields




### -field NumScopes

Integer that specifies the number of subnet statistics in <i>ScopeStats</i>.


### -field ScopeStats

Pointer to a list of <a href="https://msdn.microsoft.com/edb099a6-18eb-49b1-8f97-7f0b32a2430a">DHCPV6_STATELESS_SCOPE_STATS</a> structures.


### -field ScopeStats.size_is

 


### -field ScopeStats.size_is.NumScopes

 




## -see-also




<a href="https://msdn.microsoft.com/edb099a6-18eb-49b1-8f97-7f0b32a2430a">DHCPV6_STATELESS_SCOPE_STATS</a>



<a href="https://msdn.microsoft.com/4f6ba79c-5ab5-4d89-907d-83bdddbd09a2">DhcpV6GetStatelessStatistics</a>
 

 

