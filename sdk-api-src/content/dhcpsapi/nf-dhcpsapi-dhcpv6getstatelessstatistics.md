---
UID: NF:dhcpsapi.DhcpV6GetStatelessStatistics
title: DhcpV6GetStatelessStatistics function (dhcpsapi.h)
description: Retrieves the stateless server IPv6 subnet statistics.
helpviewer_keywords: ["DhcpV6GetStatelessStatistics","DhcpV6GetStatelessStatistics function [DHCP]","dhcp.dhcpv6getstatelessstatistics","dhcpsapi/DhcpV6GetStatelessStatistics"]
old-location: dhcp\dhcpv6getstatelessstatistics.htm
tech.root: DHCP
ms.assetid: 4f6ba79c-5ab5-4d89-907d-83bdddbd09a2
ms.date: 12/05/2018
ms.keywords: DhcpV6GetStatelessStatistics, DhcpV6GetStatelessStatistics function [DHCP], dhcp.dhcpv6getstatelessstatistics, dhcpsapi/DhcpV6GetStatelessStatistics
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpV6GetStatelessStatistics
 - dhcpsapi/DhcpV6GetStatelessStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpV6GetStatelessStatistics
---

# DhcpV6GetStatelessStatistics function


## -description

The <b>DhcpV6GetStatelessStatistics</b> function retrieves the stateless server IPv6 subnet statistics.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param StatelessStats [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_stats">DHCPV6_STATELESS_STATS</a> structure that contain DHCPv6 stateless server IPv6 subnet statistics.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

<i>StatelessStats</i> and its member, <b>ScopeStats</b>, should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6getstatelessstoreparams">DhcpV6GetStatelessStoreParams</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6setstatelessstoreparams">DhcpV6SetStatelessStoreParams</a>