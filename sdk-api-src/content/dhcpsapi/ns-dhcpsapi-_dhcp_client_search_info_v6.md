---
UID: NS:dhcpsapi._DHCP_CLIENT_SEARCH_INFO_V6
title: "_DHCP_CLIENT_SEARCH_INFO_V6"
author: windows-driver-content
description: Contains the term or value on which the DHCPv6 server database will be searched.
old-location: dhcp\dhcp_search_info_v6.htm
old-project: DHCP
ms.assetid: b290baab-9a70-437a-a519-876891184fbc
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*LPDHCP_SEARCH_INFO_V6, DHCP_SEARCH_INFO_V6, DHCP_SEARCH_INFO_V6 structure [DHCP], Dhcpv6ClientDUID, Dhcpv6ClientIpAddress, Dhcpv6ClientName, PDHCP_SEARCH_INFO_V6, PDHCP_SEARCH_INFO_V6 structure pointer [DHCP], _DHCP_CLIENT_SEARCH_INFO_V6, dhcp.dhcp_search_info_v6, dhcpsapi/DHCP_SEARCH_INFO_V6, dhcpsapi/PDHCP_SEARCH_INFO_V6"
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
req.typenames: DHCP_SEARCH_INFO_V6, *LPDHCP_SEARCH_INFO_V6
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SEARCH_INFO_V6
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_SEARCH_INFO_V6 structure


## -description


The <b>DHCP_SEARCH_INFO_V6</b> structure contains the term or value on which the DHCPv6 server database will be searched.


## -struct-fields




### -field SearchType

Enumeration value that selects the type of the value on which the DHCPv6 database will be searched.



##### )



#####  )



##### )


### -field SearchInfo.ClientIpAddress.case

 


### -field SearchInfo.ClientIpAddress.case.Dhcpv6ClientIpAddress

 


### -field SearchInfo.ClientDUID.case

 


### -field SearchInfo.ClientDUID.case.Dhcpv6ClientDUID

 


### -field SearchInfo.ClientName.case

 


### -field SearchInfo.ClientName.case.Dhcpv6ClientName

 


### -field SearchInfo.switch_is

 


### -field SearchInfo.switch_is.SearchType

 


### -field SearchInfo.switch_type

 


### -field SearchInfo.switch_type.DHCP_SEARCH_INFO_TYPE_V6

 


### -field SearchInfo


### -field SearchInfo.ClientIpAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the client IPv6 address to search for.


### -field SearchInfo.ClientDUID

GUID value that specifies the client DHCP UID to search for.


### -field SearchInfo.ClientName

Unicode string that specifies the client name to search for.


### -field _DHCP_CLIENT_SEARCH_UNION_V6

 




## -see-also




<a href="https://msdn.microsoft.com/56c2cbda-4af5-4f28-9b1f-be7d6cf0c1f5">DHCP_SEARCH_INFO_TYPE_V6</a>
 

 

