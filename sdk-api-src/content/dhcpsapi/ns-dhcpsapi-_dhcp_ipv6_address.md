---
UID: NS:dhcpsapi._DHCP_IPV6_ADDRESS
title: "_DHCP_IPV6_ADDRESS"
author: windows-sdk-content
description: DHCP_IPV6_ADDRESS structure contains an IPv6 address.
old-location: dhcp\dhcp_ipv6_address.htm
old-project: DHCP
ms.assetid: 9623e866-81e5-4d5a-8801-33f0f8973ed3
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_IPV6_ADDRESS, *PDHCP_IPV6_ADDRESS, DHCP_IPV6_ADDRESS, DHCP_IPV6_ADDRESS structure [DHCP], DHCP_RESUME_IPV6_HANDLE, DHCP_RESUME_IPV6_HANDLE structure [DHCP], LPDHCP_IPV6_ADDRESS, LPDHCP_IPV6_ADDRESS structure pointer [DHCP], PDHCP_IPV6_ADDRESS, PDHCP_IPV6_ADDRESS structure pointer [DHCP], _DHCP_IPV6_ADDRESS, dhcp.dhcp_ipv6_address, dhcpsapi/DHCP_IPV6_ADDRESS, dhcpsapi/DHCP_RESUME_IPV6_HANDLE, dhcpsapi/LPDHCP_IPV6_ADDRESS, dhcpsapi/PDHCP_IPV6_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_IPV6_ADDRESS, *LPDHCP_IPV6_ADDRESS, *PDHCP_IPV6_ADDRESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_IPV6_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_IPV6_ADDRESS structure


## -description


The 	<b>DHCP_IPV6_ADDRESS</b> structure contains an IPv6 address.


## -struct-fields




### -field HighOrderBits

A <b>ULONGULONG</b> value containing the higher 64 bits of the IPv6 address.


### -field LowOrderBits

A <b>ULONGULONG</b> value containing the lower 64 bits of the IPv6 address.


## -remarks



An alternate name for this structure is <b>DHCP_RESUME_IPV6_HANDLE</b>.



