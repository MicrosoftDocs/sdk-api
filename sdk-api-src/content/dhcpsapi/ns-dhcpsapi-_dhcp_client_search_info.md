---
UID: NS:dhcpsapi._DHCP_CLIENT_SEARCH_INFO
title: "_DHCP_CLIENT_SEARCH_INFO"
author: windows-driver-content
description: The DHCP_SEARCH_INFO structure defines the DHCP client record data used to search against for particular server operations.
old-location: dhcp\dhcp_search_info.htm
old-project: DHCP
ms.assetid: 3c6f85d7-c156-4379-bad9-0705698f12e5
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCP_SEARCH_INFO, DHCP_SEARCH_INFO, DHCP_SEARCH_INFO structure [DHCP], LPDHCP_SEARCH_INFO, LPDHCP_SEARCH_INFO structure pointer [DHCP], _DHCP_CLIENT_SEARCH_INFO, dhcp.dhcp_search_info, dhcpsapi/LPDHCP_SEARCH_INFO, dhcpsapi/_DHCP_CLIENT_SEARCH_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_SEARCH_INFO, *LPDHCP_SEARCH_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SEARCH_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_SEARCH_INFO structure


## -description


The <b>DHCP_SEARCH_INFO</b> structure defines the DHCP client record data used to search against for particular server operations.


## -struct-fields




### -field SearchInfo



#### ClientIpAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies a client IP address. This field is populated if <b>SearchType</b> is set to <b>DhcpClientIpAddress</b>.



#### ClientHardwareAddress


<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a> structure that contains a hardware MAC address.  This field is populated if <b>SearchType</b> is set to <b>DhcpClientHardwareAddress</b>.



#### ClientName

Unicode string that specifies the network name of the DHCP client.  This field is populated if <b>SearchType</b> is set to <b>DhcpClientName</b>.


### -field _DHCP_CLIENT_SEARCH_UNION

 


### -field SearchType


<a href="https://msdn.microsoft.com/b635ea03-689c-4471-bff2-72fceec78440">DHCP_SEARCH_INFO_TYPE</a> enumeration value that specifies the data included in the subsequent member of this structure.


## -see-also




<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a>



<a href="https://msdn.microsoft.com/b635ea03-689c-4471-bff2-72fceec78440">DHCP_SEARCH_INFO_TYPE</a>
 

 

