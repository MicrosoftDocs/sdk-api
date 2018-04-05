---
UID: NF:dhcpsapi.DhcpV6GetStatelessStatistics
title: DhcpV6GetStatelessStatistics function
author: windows-driver-content
description: Retrieves the stateless server IPv6 subnet statistics.
old-location: dhcp\dhcpv6getstatelessstatistics.htm
old-project: DHCP
ms.assetid: 4f6ba79c-5ab5-4d89-907d-83bdddbd09a2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DhcpV6GetStatelessStatistics, DhcpV6GetStatelessStatistics function [DHCP], dhcp.dhcpv6getstatelessstatistics, dhcpsapi/DhcpV6GetStatelessStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpV6GetStatelessStatistics
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV6GetStatelessStatistics function


## -description


The <b>DhcpV6GetStatelessStatistics</b> function retrieves the stateless server IPv6 subnet statistics.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param StatelessStats [out]

Pointer to a <a href="https://msdn.microsoft.com/8C0E26F3-9496-497C-9E05-9995CC322189">DHCPV6_STATELESS_STATS</a> structure that contain DHCPv6 stateless server IPv6 subnet statistics.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



<i>StatelessStats</i> and its member, <b>ScopeStats</b>, should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/80a32132-a032-452f-9438-52a1eb280fdf">DhcpV6GetStatelessStoreParams</a>



<a href="https://msdn.microsoft.com/8f64c1bb-8f02-45e3-b9ed-8fce2bf9885c">DhcpV6SetStatelessStoreParams</a>
 

 

