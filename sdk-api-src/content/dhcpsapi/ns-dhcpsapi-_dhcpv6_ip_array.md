---
UID: NS:dhcpsapi._DHCPV6_IP_ARRAY
title: "_DHCPV6_IP_ARRAY"
author: windows-driver-content
description: The DHCPV6_IP_ARRAY structure contains an array of DHCP IPv6 address structures.
old-location: dhcp\dhcpv6_ip_array.htm
old-project: DHCP
ms.assetid: B87CF991-FFC8-4CB4-8EE9-66716EC9B58D
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCPV6_IP_ARRAY, DHCPV6_IP_ARRAY, DHCPV6_IP_ARRAY structure [DHCP], PDHCPV6_IP_ARRAY, PDHCPV6_IP_ARRAY structure pointer [DHCP], _DHCPV6_IP_ARRAY, dhcp.dhcpv6_ip_array, dhcpsapi/DHCPV6_IP_ARRAY, dhcpsapi/PDHCPV6_IP_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: DHCPV6_IP_ARRAY, *LPDHCPV6_IP_ARRAY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCPV6_IP_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCPV6_IP_ARRAY structure


## -description


The <b>DHCPV6_IP_ARRAY</b> structure contains an array of DHCP IPv6 address structures.


## -struct-fields




### -field NumElements

The number of elements in <b>Elements</b>.


### -field Elements

An array of <a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structures.

