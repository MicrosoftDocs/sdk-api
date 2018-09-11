---
UID: NS:dhcpsapi._DHCP_IP_RANGE_V6
title: "_DHCP_IP_RANGE_V6"
author: windows-sdk-content
description: Specifies a range of IPv6 addresses for use with a DHCPv6 server.
old-location: dhcp\dhcp_ip_range_v6.htm
tech.root: dhcp
ms.assetid: 3a918a2b-beff-4562-9c7f-acee2cc8f2da
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_IP_RANGE_V6, DHCP_IP_RANGE_V6, DHCP_IP_RANGE_V6 structure [DHCP], PDHCP_IP_RANGE_V6, PDHCP_IP_RANGE_V6 structure pointer [DHCP], _DHCP_IP_RANGE_V6, dhcp.dhcp_ip_range_v6, dhcpsapi/DHCP_IP_RANGE_V6, dhcpsapi/PDHCP_IP_RANGE_V6"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Dhcpsapi.h
api_name:
 - DHCP_IP_RANGE_V6
product: Windows
targetos: Windows
req.typenames: DHCP_IP_RANGE_V6, *LPDHCP_IP_RANGE_V6
req.redist: 
---

# _DHCP_IP_RANGE_V6 structure


## -description


The <b>DHCP_IP_RANGE_V6</b> structure specifies a range of IPv6 addresses for use with a DHCPv6 server.


## -struct-fields




### -field StartAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the first IPv6 address in the range.


### -field EndAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the last IPv6 address in the range.


## -see-also




<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a>
 

 

