---
UID: NS:dhcpsapi._DHCP_HOST_INFO_V6
title: "_DHCP_HOST_INFO_V6"
author: windows-driver-content
description: Contains network information about a DHCPv6 server (host), such as its IPv6 address and name.
old-location: dhcp\dhcp_host_info_v6.htm
old-project: DHCP
ms.assetid: 7473bbcd-d032-4f44-96e8-e08f050c08a3
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCP_HOST_INFO_V6, DHCP_HOST_INFO_V6, DHCP_HOST_INFO_V6 structure [DHCP], PDHCP_HOST_INFO_V6, PDHCP_HOST_INFO_V6 structure pointer [DHCP], _DHCP_HOST_INFO_V6, dhcp.dhcp_host_info_v6, dhcpsapi/DHCP_HOST_INFO_V6, dhcpsapi/PDHCP_HOST_INFO_V6"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DHCP_HOST_INFO_V6, *LPDHCP_HOST_INFO_V6
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_HOST_INFO_V6
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_HOST_INFO_V6 structure


## -description


The <b>DHCP_HOST_INFO_V6</b> structure contains network information about a DHCPv6 server (host), such as its IPv6 address and name.


## -struct-fields




### -field IpAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address of the DHCPv6 server.


### -field NetBiosName

Pointer to a Unicode string that contains the NetBIOS name of the DHCPv6 server.


### -field HostName

Pointer to a Unicode string that contains the network name of the DHCPv6 server.


## -remarks



When this structure is populated by the DHCP Server, the <b>HostName</b> and <b>NetBiosName</b> members may be set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a>
 

 

